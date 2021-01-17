---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: e59ce4f5e3b0f1b07744e0754cf0e1cae3de7da6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427067"
---
# <span data-ttu-id="f0e92-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="f0e92-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="f0e92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0e92-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e92-103">Obter o status da replicação</span><span class="sxs-lookup"><span data-stu-id="f0e92-103">Get the status of the replication</span></span>

## <span data-ttu-id="f0e92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0e92-104">SYNTAX</span></span>

### <span data-ttu-id="f0e92-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f0e92-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e92-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0e92-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0e92-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0e92-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0e92-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0e92-108">DESCRIPTION</span></span>
<span data-ttu-id="f0e92-109">Obter o status da replicação</span><span class="sxs-lookup"><span data-stu-id="f0e92-109">Get the status of the replication</span></span>

## <span data-ttu-id="f0e92-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0e92-110">EXAMPLES</span></span>

### <span data-ttu-id="f0e92-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0e92-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="f0e92-112">Esse comando obtém o status de replicação no MyVol</span><span class="sxs-lookup"><span data-stu-id="f0e92-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="f0e92-113">OS</span><span class="sxs-lookup"><span data-stu-id="f0e92-113">PARAMETERS</span></span>

### <span data-ttu-id="f0e92-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f0e92-114">-AccountName</span></span>
<span data-ttu-id="f0e92-115">O nome da conta ANF do volume de destino de replicação</span><span class="sxs-lookup"><span data-stu-id="f0e92-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="f0e92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e92-116">-DefaultProfile</span></span>
<span data-ttu-id="f0e92-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0e92-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0e92-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0e92-118">-InputObject</span></span>
<span data-ttu-id="f0e92-119">O objeto volume de destino de replicação do ANF para obter o status de replicação</span><span class="sxs-lookup"><span data-stu-id="f0e92-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="f0e92-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0e92-120">-Name</span></span>
<span data-ttu-id="f0e92-121">O nome do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="f0e92-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="f0e92-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f0e92-122">-PoolName</span></span>
<span data-ttu-id="f0e92-123">O nome do pool ANF do volume de destino de replicação</span><span class="sxs-lookup"><span data-stu-id="f0e92-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="f0e92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0e92-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0e92-125">O grupo de recursos do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="f0e92-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="f0e92-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0e92-126">-ResourceId</span></span>
<span data-ttu-id="f0e92-127">A ID do recurso do volume de destino de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="f0e92-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="f0e92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e92-128">CommonParameters</span></span>
<span data-ttu-id="f0e92-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e92-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0e92-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e92-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0e92-131">INPUTS</span></span>

### <span data-ttu-id="f0e92-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f0e92-132">System.String</span></span>

### <span data-ttu-id="f0e92-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f0e92-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f0e92-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0e92-134">OUTPUTS</span></span>

### <span data-ttu-id="f0e92-135">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="f0e92-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="f0e92-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0e92-136">NOTES</span></span>

## <span data-ttu-id="f0e92-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0e92-137">RELATED LINKS</span></span>
