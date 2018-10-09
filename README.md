# alximik
#include <windows.h>
#include <math.h>

const wchar_t windowClass[] = L"win32app";
const wchar_t windowTitle[] = L"Win32API - Пример окна";
int  x_2, y_2 , x_1, y_1, n = 1, n_1 = 0, n_2 = 0;
//const double PI = 3.1415926535897932384626433832795;
#define M_PI      3.14159265358979323846   

void BACKGROUND(HDC hdc, RECT r) {
	HBRUSH brush, old_brush;
	brush = CreateSolidBrush(RGB(187, 187, 187));
	old_brush = (HBRUSH)SelectObject(hdc, brush);
	//Polygon(hdc, pt, 5);
	Rectangle(hdc, 0, 0, r.right, r.bottom);
	/* if (n_1 == 1) {
		 Rectangle(hdc, x_2, y_2, 250 + x_2, 150 + y_2);
	 }*/
	 // Polygon(hdc, pt,4);
	   //Ellipse(hdc, 100+y_1, 100+x_1, 400 + y_1, 400 + x_1);
	SelectObject(hdc, old_brush);
	DeleteObject(brush);

}

void DrawingGrid(HDC hdc, RECT r) {
	HPEN pen, old_pen;
	pen = CreatePen(PS_SOLID, 1.5, RGB(0, 0, 255));
	old_pen = (HPEN)SelectObject(hdc, pen);
	for (int q_1_1 = 7, q_2_2 = 12, q_3_3 = 12; q_1_1 < r.bottom, q_2_2 < r.bottom, q_3_3 < r.bottom; q_1_1 += 25, q_2_2 += 25, q_3_3 += 25) {
		for (int q_1 = 15, q_2 = 11, q_3 = 19; q_1 < r.right, q_2 < r.right, q_3 < r.right; q_1 += 25, q_2 += 25, q_3 += 25) {
			MoveToEx(hdc, q_1, q_1_1, NULL);
			q_1 += 3;
			LineTo(hdc, q_1, q_1_1);
			MoveToEx(hdc, q_2, q_2_2, NULL);
			q_2 += 3;
			LineTo(hdc, q_2, q_2_2);
			MoveToEx(hdc, q_3, q_2_2, NULL);
			q_3 += 3;
			LineTo(hdc, q_3, q_2_2);
		}
	}
	SelectObject(hdc, old_pen);
	DeleteObject(pen);


}

void Element_1(HDC hdc, int x, int y, int n_2_2) {
	if (n_2_2== 1) {

		HBRUSH brush, old_brush;
		HPEN pen, old_pen;
		brush = CreateSolidBrush(RGB(255, 0, 0));
		old_brush = (HBRUSH)SelectObject(hdc, brush);
		Rectangle(hdc, x, y + 60, x + 15, y + 60 + 15);
		Rectangle(hdc, x, y, x + 15, y + 15);
		pen = CreatePen(PS_SOLID, 2, RGB(0, 128, 0));
		old_pen = (HPEN)SelectObject(hdc, pen);

		
		//Polygon(hdc, pt, 5);
		
		/* if (n_1 == 1) {
			 Rectangle(hdc, x_2, y_2, 250 + x_2, 150 + y_2);
		 }*/
		 // Polygon(hdc, pt,4);
		   //Ellipse(hdc, 100+y_1, 100+x_1, 400 + y_1, 400 + x_1);



		MoveToEx(hdc, x + 7.5, y +15, NULL);
		LineTo(hdc, x + 7.5, y + 60);
		
		MoveToEx(hdc, x, y + 40, NULL);
		LineTo(hdc, x + 13, y + 40);
		MoveToEx(hdc, x + 13, y + 40, NULL);
		LineTo(hdc, x + 7, y + 48);
		MoveToEx(hdc, x, y + 40, NULL);
		LineTo(hdc, x + 7, y + 48);


		MoveToEx(hdc, x-3, y + 40, NULL);
		LineTo(hdc, x -8, y + 40);
		MoveToEx(hdc, x -8, y + 40, NULL);
		LineTo(hdc, x - 8, y + 32);
		MoveToEx(hdc, x - 8, y + 32, NULL);
		LineTo(hdc, x -12, y + 32);
		MoveToEx(hdc, x - 12, y + 40, NULL);
		LineTo(hdc, x - 12, y + 32);
		MoveToEx(hdc, x - 12, y + 40, NULL);
		LineTo(hdc, x - 18, y + 40);
		MoveToEx(hdc, x - 18, y + 40, NULL);
		LineTo(hdc, x - 18, y + 32);
		MoveToEx(hdc, x - 18, y + 32, NULL);
		LineTo(hdc, x - 24, y + 32);
		MoveToEx(hdc, x - 22, y + 32, NULL);
		LineTo(hdc, x - 22, y + 40);
		MoveToEx(hdc, x - 22, y + 40, NULL);
		LineTo(hdc, x - 28, y + 40);


		SelectObject(hdc, old_brush);
		DeleteObject(brush);
		Arc(hdc, x - 4, y + 28, x + 19, y + 48, x, y + 30, x, y + 30);

		//Ellipse(hdc, 100 + y, 100 + x, 400 + y, 400 + x);
		SelectObject(hdc, old_pen);
		DeleteObject(pen);
	}
}

void Element_2(HDC hdc, int x, int y,int n_1_1) {
	if (n_1_1 == 1) {
		HBRUSH brush, old_brush;
		HPEN pen, old_pen;
		brush = CreateSolidBrush(RGB(255, 0, 0));
		old_brush = (HBRUSH)SelectObject(hdc, brush);
		Rectangle(hdc, x, y + 60, x + 15, y + 60 + 15);
		Rectangle(hdc, x, y, x + 15, y + 15);
		pen = CreatePen(PS_SOLID, 2, RGB(0, 128, 0));
		old_pen = (HPEN)SelectObject(hdc, pen);
		MoveToEx(hdc, x + 7.5, y + 15, NULL);
		LineTo(hdc, x + 7.5, y + 26.25);
		MoveToEx(hdc, x -5, y + 26.25, NULL);
		LineTo(hdc, x + 20, y + 26.25);
		MoveToEx(hdc, x - 5, y + 26.25, NULL);
		LineTo(hdc, x + 7.5, y + 37.5);
		MoveToEx(hdc, x +20, y + 26.25, NULL);
		LineTo(hdc, x + 7.5, y + 37.5);
		MoveToEx(hdc, x -8, y + 37.5, NULL);
		LineTo(hdc, x +23, y + 37.5);
		MoveToEx(hdc, x + 7.5, y + 37.5, NULL);
		LineTo(hdc, x + 7.5, y + 60);

		SelectObject(hdc, old_brush);
		DeleteObject(brush);
		//Ellipse(hdc, 100 + y, 100 + x, 400 + y, 400 + x);
		SelectObject(hdc, old_pen);
		DeleteObject(pen);
	}

}

void Cosinus(HDC hdc, RECT r) {
	HBRUSH brush, old_brush;
	HPEN pen, old_pen;
	//HPEN pen_cos, old_pen_cos;
	brush = CreateSolidBrush(RGB(73,66,61));
	old_brush = (HBRUSH)SelectObject(hdc, brush);
	pen = CreatePen(PS_DOT, 1, RGB(187, 187, 187));
	
	old_pen = (HPEN)SelectObject(hdc, pen);
	Rectangle(hdc, r.right / 2, r.bottom / 2, r.right, r.bottom);
	float x = 0, y;
	for (int y_scr,x_scr; x < 10* M_PI; x += 0.01) {
	
		y = cos(x+ M_PI);
		y_scr = (((y*r.bottom/2)/2)+r.bottom/2+ r.bottom/4);
			x_scr = (((x* r.right / 2)/(10* M_PI)) +r.right/2);

		SetPixel(hdc, x_scr, y_scr, RGB(255, 255, 0));
	}
	SelectObject(hdc, old_brush);
	DeleteObject(brush);
	SelectObject(hdc, old_pen);
	DeleteObject(pen);
}

long __stdcall WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam) {

	PAINTSTRUCT ps;
	HDC hdc;
	POINT pt[4] = { {x_1, y_1}, {100 + x_1,200 + y_1}, {400 + x_1,5 + y_1} , { 900 + x_1,100 + y_1 } };

	RECT r;
	GetClientRect(hWnd, &r);
	HPEN pen, old_pen;
	HBRUSH brush, old_brush;


	switch (message) {
	case WM_DESTROY:
		PostQuitMessage(0);
		break;
	case WM_LBUTTONDOWN:
		if (wParam & MK_CONTROL) {
			if ((r.left + 8 < LOWORD(lParam) && LOWORD(lParam) < r.right - 23) && (r.top < HIWORD(lParam) && HIWORD(lParam) < r.bottom - 75)) {
				x_2 = LOWORD(lParam);
				y_2 = HIWORD(lParam);
				InvalidateRect(hWnd, NULL, true);
				n_1 = 1;
			}
		}
		else {
			if ((r.left + 28 < LOWORD(lParam) && LOWORD(lParam) < r.right - 19) && (r.top < HIWORD(lParam) && HIWORD(lParam) < r.bottom - 75)) {
				x_1 = LOWORD(lParam);
				y_1 = HIWORD(lParam);
				InvalidateRect(hWnd, NULL, true);
				n_2 = 1;
			}
		}
		break;
	case WM_KEYDOWN:
		/*if ((y_2 + 75 <r.bottom || x_2 +23 <r.right || y_2 >r.top || x_2 - 8 > r.left) || (y_1 + 75 < r.bottom || x_1 + 19 < r.right || y_1 > r.top || x_1-28 > r.left)){*/
			if (wParam == VK_DOWN && y_2 + 75 < r.bottom && y_1 + 75 < r.bottom) {
				y_2 += 1;
				y_1 += 1;
			}

		if (wParam == VK_UP && y_2 > r.top && y_1 > r.top) {
			y_2 -= 1;
			y_1 -= 1;
		}
		if (wParam == VK_LEFT && x_2 - 8 > r.left && x_1 - 28 > r.left) {
			x_2 -= 1;
			x_1 -= 1;
		}
		if (wParam == VK_RIGHT && x_1 + 19 < r.right  && x_2 + 23 < r.right) {
			x_2 += 1;
			x_1 += 1;
		}
		InvalidateRect(hWnd, NULL, true);
	//}

		
		break;
	case WM_TIMER:
		/*  if (wParam == 33) {

			  y += n;
		  }
		  if (y == 750) {
			  n = -1;
		  }
		  if (y == 0) {
			  n = 1;
		  }

		  else {
			  x_2 += 1;
		  }*/

		  /*InvalidateRect(hWnd, NULL, true);*/
		break;
	case WM_PAINT:
		hdc = BeginPaint(hWnd, &ps);

		/*TextOut(hdc, 0, 0, L"ПКИМС рулит!", 12);*/
	   // pen = CreatePen(PS_SOLID, 5, RGB(148, 0, 211));
	   // old_pen = (HPEN)SelectObject(hdc, pen);
	   // brush = CreateSolidBrush(RGB(187, 187, 187));
	   // old_brush = (HBRUSH)SelectObject(hdc, brush);
		//Polygon(hdc, pt, 5);
		//Rectangle(hdc, x, y, r.right, r.bottom);
		/* if (n_1 == 1) {
			 Rectangle(hdc, x_2, y_2, 250 + x_2, 150 + y_2);
		 }*/
		 // Polygon(hdc, pt,4);
		   //Ellipse(hdc, 100+y_1, 100+x_1, 400 + y_1, 400 + x_1);
		//SelectObject(hdc, old_brush);
		BACKGROUND(hdc, r);
		DrawingGrid(hdc, r);
		Element_1(hdc, x_1, y_1, n_2);
		Element_2(hdc, x_2, y_2,n_1);
		Cosinus(hdc, r);
		//SetPixel(hdc,34, 34, RGB(255, 255, 0));
		// Rectangle(hdc, 50, 50, 250, 150);
		 /*SelectObject(hdc, old_pen);
		 DeleteObject(pen);*/

		 /* Ellipse(hdc, 100, 100, 400, 400);
		  MoveToEx(hdc, 99, 400, NULL);
		  LineTo(hdc,900, 900);
		  LineTo(hdc, 200, 99);
		  Polygon(hdc, pt, 5);
		  SetPixel(hdc, 340, 888, RGB(456, 100, 45));*/
		EndPaint(hWnd, &ps);

		break;
		/* if (x == x_2 && y == y_2) {
			 MessageBox(hWnd, L"Пересек", L"Внимание сообщение", MB_YESNO | MB_ICONQUESTION);
		 }*/
		 /*case WM_LBUTTONDOWN:
			 MessageBox(hWnd, L"Нажата левая клавиша мыши!", L"Внимание сообщение", MB_OK|MB_ICONQUESTION);*/
	case WM_CLOSE:
		if (MessageBox(hWnd, L"Выйти из программы?", L"Внимание сообщение", MB_YESNO | MB_ICONQUESTION) == IDNO) {
			return 0;
		}
		else
			return DefWindowProc(hWnd, message, wParam, lParam);
		break;



	default:
		return DefWindowProc(hWnd, message, wParam, lParam);
	}
	return 0;
}

int __stdcall WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) {
	WNDCLASSEX wcex;

	wcex.cbSize = sizeof(WNDCLASSEX);
	wcex.style = CS_HREDRAW | CS_VREDRAW;
	wcex.lpfnWndProc = WndProc;
	wcex.cbClsExtra = 0;
	wcex.cbWndExtra = 0;
	wcex.hInstance = hInstance;
	wcex.hIcon = LoadIcon(hInstance, MAKEINTRESOURCE(IDI_APPLICATION));
	wcex.hCursor = LoadCursor(NULL, IDC_ARROW);
	wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW + 1);
	wcex.lpszMenuName = NULL;
	wcex.lpszClassName = windowClass;
	wcex.hIconSm = LoadIcon(wcex.hInstance, MAKEINTRESOURCE(IDI_APPLICATION));

	if (!RegisterClassEx(&wcex)) {
		MessageBox(NULL, L"CanТt register window class!", L"Win32 API Test", NULL);
		return 1;
	}

	HWND hWnd = CreateWindow(windowClass, windowTitle, WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 500, 400, NULL, NULL, hInstance, NULL);

	if (!hWnd) {
		MessageBox(NULL, L"CanТt create window!", L"Win32 API Test", NULL);
		return 1;
	}

	ShowWindow(hWnd, nCmdShow);
	UpdateWindow(hWnd);
	SetTimer(hWnd, 33, 10, NULL);
	SetTimer(hWnd, 34, 10, NULL);
	MSG msg;

	while (GetMessage(&msg, NULL, 0, 0)) {
		TranslateMessage(&msg);
		DispatchMessage(&msg);
	}
	KillTimer(hWnd, 33);
	KillTimer(hWnd, 34);
	return msg.wParam;
}
