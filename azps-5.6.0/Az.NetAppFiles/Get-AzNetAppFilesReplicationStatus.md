---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: 73efd000f6889675c3daf9f99821640a8b6fbb99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887462"
---
# <span data-ttu-id="c1d73-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="c1d73-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="c1d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1d73-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d73-103">Obter o status da replicação</span><span class="sxs-lookup"><span data-stu-id="c1d73-103">Get the status of the replication</span></span>

## <span data-ttu-id="c1d73-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c1d73-104">SYNTAX</span></span>

### <span data-ttu-id="c1d73-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c1d73-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1d73-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1d73-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1d73-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1d73-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1d73-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c1d73-108">DESCRIPTION</span></span>
<span data-ttu-id="c1d73-109">Obter o status da replicação</span><span class="sxs-lookup"><span data-stu-id="c1d73-109">Get the status of the replication</span></span>

## <span data-ttu-id="c1d73-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1d73-110">EXAMPLES</span></span>

### <span data-ttu-id="c1d73-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1d73-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="c1d73-112">Este comando obtém o status da replicação em MyVol</span><span class="sxs-lookup"><span data-stu-id="c1d73-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="c1d73-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c1d73-113">PARAMETERS</span></span>

### <span data-ttu-id="c1d73-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1d73-114">-AccountName</span></span>
<span data-ttu-id="c1d73-115">O nome da conta ANF do volume de destino de replicação</span><span class="sxs-lookup"><span data-stu-id="c1d73-115">The name of the ANF account of the replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1d73-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d73-116">-DefaultProfile</span></span>
<span data-ttu-id="c1d73-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1d73-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1d73-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1d73-118">-InputObject</span></span>
<span data-ttu-id="c1d73-119">O objeto de volume de destino de replicação ANF para obter o status de replicação</span><span class="sxs-lookup"><span data-stu-id="c1d73-119">The ANF replication destination volume object to get replication status</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1d73-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c1d73-120">-Name</span></span>
<span data-ttu-id="c1d73-121">O nome do volume de destino de replicação ANF</span><span class="sxs-lookup"><span data-stu-id="c1d73-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1d73-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c1d73-122">-PoolName</span></span>
<span data-ttu-id="c1d73-123">O nome do pool ANF do volume de destino de replicação</span><span class="sxs-lookup"><span data-stu-id="c1d73-123">The name of the ANF pool of the replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1d73-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1d73-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1d73-125">O grupo de recursos do volume de destino de replicação ANF</span><span class="sxs-lookup"><span data-stu-id="c1d73-125">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1d73-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d73-126">-ResourceId</span></span>
<span data-ttu-id="c1d73-127">A id de recurso do volume de destino de replicação ANF</span><span class="sxs-lookup"><span data-stu-id="c1d73-127">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1d73-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d73-128">CommonParameters</span></span>
<span data-ttu-id="c1d73-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1d73-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d73-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1d73-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d73-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1d73-131">INPUTS</span></span>

### <span data-ttu-id="c1d73-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c1d73-132">System.String</span></span>

### <span data-ttu-id="c1d73-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c1d73-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c1d73-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c1d73-134">OUTPUTS</span></span>

### <span data-ttu-id="c1d73-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="c1d73-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="c1d73-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="c1d73-136">NOTES</span></span>

## <span data-ttu-id="c1d73-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1d73-137">RELATED LINKS</span></span>
