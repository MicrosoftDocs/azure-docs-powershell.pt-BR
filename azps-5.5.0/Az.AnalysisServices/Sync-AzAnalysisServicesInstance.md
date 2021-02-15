---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112312"
---
# <span data-ttu-id="88258-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="88258-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="88258-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88258-102">SYNOPSIS</span></span>

<span data-ttu-id="88258-103">Sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services com todas as instâncias de escala de consulta no Ambiente conectado no momento, conforme especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="88258-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="88258-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88258-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88258-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="88258-105">DESCRIPTION</span></span>

<span data-ttu-id="88258-106">O cmdlet Sync-AzAnalysisServicesInstance sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services com todas as instâncias de escala de consulta no Ambiente atualmente conectado, conforme especificado no comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="88258-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="88258-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="88258-107">EXAMPLES</span></span>

### <span data-ttu-id="88258-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88258-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="88258-109">Esse comando sincroniza o banco de dados chamado SalesOrders no servidor chamado "contoso" no ambiente westus.asazure.windows.net desde que o usuário tenha se conectado a esse ambiente usando o comando Add-AzAnalysisServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="88258-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="88258-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88258-110">PARAMETERS</span></span>

### <span data-ttu-id="88258-111">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="88258-111">-Database</span></span>

<span data-ttu-id="88258-112">Identidade do banco de dados a ser sincronizada</span><span class="sxs-lookup"><span data-stu-id="88258-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="88258-113">-Instância</span><span class="sxs-lookup"><span data-stu-id="88258-113">-Instance</span></span>

<span data-ttu-id="88258-114">Nome da instância do servidor do Analysis Services para reiniciar</span><span class="sxs-lookup"><span data-stu-id="88258-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="88258-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88258-115">-PassThru</span></span>

<span data-ttu-id="88258-116">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="88258-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="88258-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="88258-117">-Confirm</span></span>
<span data-ttu-id="88258-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88258-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88258-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88258-119">-WhatIf</span></span>
<span data-ttu-id="88258-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="88258-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88258-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88258-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88258-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88258-122">CommonParameters</span></span>
<span data-ttu-id="88258-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88258-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88258-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88258-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88258-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="88258-125">INPUTS</span></span>

### <span data-ttu-id="88258-126">System.String</span><span class="sxs-lookup"><span data-stu-id="88258-126">System.String</span></span>

## <span data-ttu-id="88258-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="88258-127">OUTPUTS</span></span>

### <span data-ttu-id="88258-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="88258-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="88258-129">Notas</span><span class="sxs-lookup"><span data-stu-id="88258-129">NOTES</span></span>

<span data-ttu-id="88258-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="88258-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="88258-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88258-131">RELATED LINKS</span></span>
