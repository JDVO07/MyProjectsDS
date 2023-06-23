# MyProjectsDS

My Scripts "M"

# This M language script creates a date calendar in Power Bi

let
    ListaFechas = Table.Column(Ventas, "Fecha"),
    FechaMin = List.Min(ListaFechas),
    FechaMax = List.Max(ListaFechas),
    Dias = Number.From(FechaMax - FechaMin)+1,
    Fechas = List.Dates(FechaMin, Dias, #duration(1,0,0,0)),
in
    Fechas

