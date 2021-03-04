---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: c5ffd95cb3bd5e902e2e9edadfa9c96dd441c744
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886289"
---
# <span data-ttu-id="7a8b9-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="7a8b9-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="7a8b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a8b9-102">SYNOPSIS</span></span>

<span data-ttu-id="7a8b9-103">Sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services a todas as instâncias de escala de consulta no ambiente atualmente conectado, conforme especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7a8b9-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="7a8b9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7a8b9-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a8b9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7a8b9-105">DESCRIPTION</span></span>

<span data-ttu-id="7a8b9-106">O cmdlet Sync-AzAnalysisServicesInstance sincroniza um banco de dados especificado na instância especificada do servidor analysis Services a todas as instâncias de dimensionar de consulta no ambiente atualmente conectado, conforme especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7a8b9-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="7a8b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a8b9-107">EXAMPLES</span></span>

### <span data-ttu-id="7a8b9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a8b9-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="7a8b9-109">Este comando sincroniza o banco de dados chamado SalesOrders no servidor chamado 'contoso' no ambiente westus.asazure.windows.net desde que o usuário tenha conectado a esse ambiente usando o comando Add-AzAnalysisServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="7a8b9-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="7a8b9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7a8b9-110">PARAMETERS</span></span>

### <span data-ttu-id="7a8b9-111">-Database</span><span class="sxs-lookup"><span data-stu-id="7a8b9-111">-Database</span></span>

<span data-ttu-id="7a8b9-112">Identidade do banco de dados a ser sincronizado</span><span class="sxs-lookup"><span data-stu-id="7a8b9-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b9-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="7a8b9-113">-Instance</span></span>

<span data-ttu-id="7a8b9-114">Nome da instância do servidor do Analysis Services a ser reiniciada</span><span class="sxs-lookup"><span data-stu-id="7a8b9-114">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a8b9-115">-PassThru</span></span>

<span data-ttu-id="7a8b9-116">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7a8b9-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a8b9-117">-Confirm</span></span>
<span data-ttu-id="7a8b9-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a8b9-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a8b9-119">-WhatIf</span></span>
<span data-ttu-id="7a8b9-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a8b9-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a8b9-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a8b9-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8b9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8b9-122">CommonParameters</span></span>
<span data-ttu-id="7a8b9-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a8b9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8b9-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a8b9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8b9-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a8b9-125">INPUTS</span></span>

### <span data-ttu-id="7a8b9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7a8b9-126">System.String</span></span>

## <span data-ttu-id="7a8b9-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7a8b9-127">OUTPUTS</span></span>

### <span data-ttu-id="7a8b9-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="7a8b9-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="7a8b9-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="7a8b9-129">NOTES</span></span>

<span data-ttu-id="7a8b9-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="7a8b9-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="7a8b9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a8b9-131">RELATED LINKS</span></span>
