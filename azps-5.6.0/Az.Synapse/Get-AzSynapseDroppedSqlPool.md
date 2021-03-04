---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedroppedsqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
ms.openlocfilehash: 26e4e5c77913f01b8a7097f6baebd68977ceed22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889115"
---
# <span data-ttu-id="baf99-101">Get-AzSynapseDroppedSqlPool</span><span class="sxs-lookup"><span data-stu-id="baf99-101">Get-AzSynapseDroppedSqlPool</span></span>

## <span data-ttu-id="baf99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baf99-102">SYNOPSIS</span></span>
<span data-ttu-id="baf99-103">Obtém um backup de pool Sql descartado de um Pool Sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="baf99-103">Gets a dropped Sql pool backup of a Synapse Sql Pool.</span></span>

## <span data-ttu-id="baf99-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="baf99-104">SYNTAX</span></span>

### <span data-ttu-id="baf99-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="baf99-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baf99-106">DroppedSqlPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="baf99-106">DroppedSqlPoolResourceId</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="baf99-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="baf99-107">DESCRIPTION</span></span>
<span data-ttu-id="baf99-108">O cmdlet **Get-AzSynapseDroppedSqlPool** obtém um backup de pool excluído especificado SQL que você pode restaurar ou todos os backups excluídos que você pode restaurar em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="baf99-108">The **Get-AzSynapseDroppedSqlPool** cmdlet gets a specified deleted SQL pool backup that you can restore, or all deleted backups that you can restore in a workspace.</span></span> 


## <span data-ttu-id="baf99-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="baf99-109">EXAMPLES</span></span>

### <span data-ttu-id="baf99-110">Exemplo 1: Obter um sqlpools descartados especificado de um pool sql</span><span class="sxs-lookup"><span data-stu-id="baf99-110">Example 1: Get a specified dropped sqlpools from a sql pool</span></span>
```powershell
PS C:\> Get-AzSynapseDroppedSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name "ContosoSqlPool"
```
<span data-ttu-id="baf99-111">O cmdlet recupera sqlpools descartados para um pool sql.</span><span class="sxs-lookup"><span data-stu-id="baf99-111">The cmdlet retrieves dropped sqlpools for a sql pool.</span></span>

### <span data-ttu-id="baf99-112">Exemplo 2: Obter todo o sqlpool descartado em um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="baf99-112">Example 2: Get all dropped sqlpool on a workspace</span></span>
```
PS C:\>Get-AzSynapseDroppedSqlPool -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="baf99-113">Esse comando obtém todo o sqlpool descartado disponível em um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="baf99-113">This command gets all available dropped sqlpool on a specified workspace.</span></span>

## <span data-ttu-id="baf99-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="baf99-114">PARAMETERS</span></span>

### <span data-ttu-id="baf99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf99-115">-DefaultProfile</span></span>
<span data-ttu-id="baf99-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="baf99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf99-117">-Name</span><span class="sxs-lookup"><span data-stu-id="baf99-117">-Name</span></span>
<span data-ttu-id="baf99-118">O pool Sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="baf99-118">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: AzSynapseDroppedSqlPool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf99-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="baf99-119">-ResourceId</span></span>
<span data-ttu-id="baf99-120">Input a Dropped Sql Pool Resource Id.</span><span class="sxs-lookup"><span data-stu-id="baf99-120">Input a Dropped Sql Pool Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DroppedSqlPoolResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf99-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf99-121">-ResourceGroupName</span></span>
<span data-ttu-id="baf99-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="baf99-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf99-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="baf99-123">-WorkspaceName</span></span>
<span data-ttu-id="baf99-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="baf99-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf99-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf99-125">CommonParameters</span></span>
<span data-ttu-id="baf99-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf99-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf99-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baf99-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf99-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="baf99-128">INPUTS</span></span>

### <span data-ttu-id="baf99-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="baf99-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="baf99-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="baf99-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="baf99-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="baf99-131">OUTPUTS</span></span>

### <span data-ttu-id="baf99-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span><span class="sxs-lookup"><span data-stu-id="baf99-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span></span>

## <span data-ttu-id="baf99-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="baf99-133">NOTES</span></span>

## <span data-ttu-id="baf99-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="baf99-134">RELATED LINKS</span></span>
