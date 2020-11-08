---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116473"
---
# <span data-ttu-id="8798c-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="8798c-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="8798c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8798c-102">SYNOPSIS</span></span>

<span data-ttu-id="8798c-103">Sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services para todas as instâncias de dimensionamento de consulta no ambiente atualmente conectado, conforme especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8798c-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8798c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8798c-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8798c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8798c-105">DESCRIPTION</span></span>

<span data-ttu-id="8798c-106">O cmdlet Sync-AzAnalysisServicesInstance sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services para todas as instâncias de dimensionamento de consulta no ambiente atualmente conectado, conforme especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8798c-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8798c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8798c-107">EXAMPLES</span></span>

### <span data-ttu-id="8798c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8798c-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="8798c-109">Esse comando sincronizará o banco de dados chamado SalesOrders no servidor chamado ' contoso ' no ambiente westus.asazure.windows.net desde que o usuário tenha se conectado nesse ambiente usando Add-AzAnalysisServicesAccount comando.</span><span class="sxs-lookup"><span data-stu-id="8798c-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="8798c-110">OS</span><span class="sxs-lookup"><span data-stu-id="8798c-110">PARAMETERS</span></span>

### <span data-ttu-id="8798c-111">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="8798c-111">-Database</span></span>

<span data-ttu-id="8798c-112">Identidade do banco de dados a ser sincronizado</span><span class="sxs-lookup"><span data-stu-id="8798c-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="8798c-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="8798c-113">-Instance</span></span>

<span data-ttu-id="8798c-114">Nome da instância do servidor do Analysis Services para reiniciar</span><span class="sxs-lookup"><span data-stu-id="8798c-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="8798c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8798c-115">-PassThru</span></span>

<span data-ttu-id="8798c-116">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8798c-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8798c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8798c-117">-Confirm</span></span>
<span data-ttu-id="8798c-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8798c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8798c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8798c-119">-WhatIf</span></span>
<span data-ttu-id="8798c-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8798c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8798c-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8798c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8798c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8798c-122">CommonParameters</span></span>
<span data-ttu-id="8798c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8798c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8798c-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8798c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8798c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8798c-125">INPUTS</span></span>

### <span data-ttu-id="8798c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8798c-126">System.String</span></span>

## <span data-ttu-id="8798c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8798c-127">OUTPUTS</span></span>

### <span data-ttu-id="8798c-128">Microsoft. Azure. Commands. AnalysisServices. dataplanting. Models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="8798c-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="8798c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8798c-129">NOTES</span></span>

<span data-ttu-id="8798c-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="8798c-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="8798c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8798c-131">RELATED LINKS</span></span>
