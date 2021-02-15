---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: e59ce4f5e3b0f1b07744e0754cf0e1cae3de7da6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114736"
---
# <span data-ttu-id="ce963-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="ce963-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="ce963-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce963-102">SYNOPSIS</span></span>
<span data-ttu-id="ce963-103">Obter o status da replicação</span><span class="sxs-lookup"><span data-stu-id="ce963-103">Get the status of the replication</span></span>

## <span data-ttu-id="ce963-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce963-104">SYNTAX</span></span>

### <span data-ttu-id="ce963-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ce963-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce963-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce963-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce963-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce963-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce963-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce963-108">DESCRIPTION</span></span>
<span data-ttu-id="ce963-109">Obter o status da replicação</span><span class="sxs-lookup"><span data-stu-id="ce963-109">Get the status of the replication</span></span>

## <span data-ttu-id="ce963-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ce963-110">EXAMPLES</span></span>

### <span data-ttu-id="ce963-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce963-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="ce963-112">Este comando obtém o status de replicação no MyVol</span><span class="sxs-lookup"><span data-stu-id="ce963-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="ce963-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce963-113">PARAMETERS</span></span>

### <span data-ttu-id="ce963-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="ce963-114">-AccountName</span></span>
<span data-ttu-id="ce963-115">O nome da conta ANF do volume de destino de replicação</span><span class="sxs-lookup"><span data-stu-id="ce963-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="ce963-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce963-116">-DefaultProfile</span></span>
<span data-ttu-id="ce963-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce963-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce963-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce963-118">-InputObject</span></span>
<span data-ttu-id="ce963-119">O objeto de volume de destino de replicação da ANF para obter o status de replicação</span><span class="sxs-lookup"><span data-stu-id="ce963-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="ce963-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce963-120">-Name</span></span>
<span data-ttu-id="ce963-121">O nome do volume de destino de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="ce963-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ce963-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ce963-122">-PoolName</span></span>
<span data-ttu-id="ce963-123">O nome do pool de ANF do volume de destino de replicação</span><span class="sxs-lookup"><span data-stu-id="ce963-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="ce963-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce963-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce963-125">O grupo de recursos do volume de destino de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="ce963-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ce963-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce963-126">-ResourceId</span></span>
<span data-ttu-id="ce963-127">A ID do recurso do volume de destino de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="ce963-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ce963-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce963-128">CommonParameters</span></span>
<span data-ttu-id="ce963-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce963-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce963-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce963-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce963-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="ce963-131">INPUTS</span></span>

### <span data-ttu-id="ce963-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ce963-132">System.String</span></span>

### <span data-ttu-id="ce963-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ce963-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ce963-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="ce963-134">OUTPUTS</span></span>

### <span data-ttu-id="ce963-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="ce963-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="ce963-136">Notas</span><span class="sxs-lookup"><span data-stu-id="ce963-136">NOTES</span></span>

## <span data-ttu-id="ce963-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce963-137">RELATED LINKS</span></span>
