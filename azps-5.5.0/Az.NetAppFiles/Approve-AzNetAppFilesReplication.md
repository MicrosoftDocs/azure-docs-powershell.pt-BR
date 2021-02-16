---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113547"
---
# <span data-ttu-id="cd8c2-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="cd8c2-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="cd8c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd8c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd8c2-103">Aprovar/autorizar a conexão de replicação no volume de origem</span><span class="sxs-lookup"><span data-stu-id="cd8c2-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="cd8c2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd8c2-104">SYNTAX</span></span>

### <span data-ttu-id="cd8c2-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cd8c2-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd8c2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd8c2-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd8c2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd8c2-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd8c2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd8c2-108">DESCRIPTION</span></span>
<span data-ttu-id="cd8c2-109">Aprovar a conexão de replicação no volume de origem</span><span class="sxs-lookup"><span data-stu-id="cd8c2-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="cd8c2-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cd8c2-110">EXAMPLES</span></span>

### <span data-ttu-id="cd8c2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd8c2-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="cd8c2-112">Este comando aprova a replicação no MyAnfVolume.</span><span class="sxs-lookup"><span data-stu-id="cd8c2-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="cd8c2-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd8c2-113">PARAMETERS</span></span>

### <span data-ttu-id="cd8c2-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="cd8c2-114">-AccountName</span></span>
<span data-ttu-id="cd8c2-115">O nome da conta ANF do volume da fonte de replicação</span><span class="sxs-lookup"><span data-stu-id="cd8c2-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="cd8c2-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="cd8c2-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="cd8c2-117">A ID do sistema de arquivos do volume de proteção de dados de destino</span><span class="sxs-lookup"><span data-stu-id="cd8c2-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="cd8c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd8c2-118">-DefaultProfile</span></span>
<span data-ttu-id="cd8c2-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd8c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd8c2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd8c2-120">-InputObject</span></span>
<span data-ttu-id="cd8c2-121">O objeto de volume de origem ANF para o destino de replicação autorizado</span><span class="sxs-lookup"><span data-stu-id="cd8c2-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="cd8c2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd8c2-122">-Name</span></span>
<span data-ttu-id="cd8c2-123">O nome do volume de origem de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="cd8c2-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="cd8c2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd8c2-124">-PassThru</span></span>
<span data-ttu-id="cd8c2-125">Retornar se a autorização de replicação do volume especificado foi executada</span><span class="sxs-lookup"><span data-stu-id="cd8c2-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="cd8c2-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="cd8c2-126">-PoolName</span></span>
<span data-ttu-id="cd8c2-127">O nome do pool ANF do volume de origem de replicação</span><span class="sxs-lookup"><span data-stu-id="cd8c2-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="cd8c2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd8c2-128">-ResourceGroupName</span></span>
<span data-ttu-id="cd8c2-129">O grupo de recursos do volume de origem de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="cd8c2-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="cd8c2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd8c2-130">-ResourceId</span></span>
<span data-ttu-id="cd8c2-131">A ID do recurso do volume de origem de replicação da ANF</span><span class="sxs-lookup"><span data-stu-id="cd8c2-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="cd8c2-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cd8c2-132">-Confirm</span></span>
<span data-ttu-id="cd8c2-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd8c2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd8c2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd8c2-134">-WhatIf</span></span>
<span data-ttu-id="cd8c2-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cd8c2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd8c2-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd8c2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd8c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd8c2-137">CommonParameters</span></span>
<span data-ttu-id="cd8c2-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd8c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd8c2-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd8c2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd8c2-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="cd8c2-140">INPUTS</span></span>

### <span data-ttu-id="cd8c2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cd8c2-141">System.String</span></span>

### <span data-ttu-id="cd8c2-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="cd8c2-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="cd8c2-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="cd8c2-143">OUTPUTS</span></span>

### <span data-ttu-id="cd8c2-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd8c2-144">System.Boolean</span></span>

## <span data-ttu-id="cd8c2-145">Notas</span><span class="sxs-lookup"><span data-stu-id="cd8c2-145">NOTES</span></span>

## <span data-ttu-id="cd8c2-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd8c2-146">RELATED LINKS</span></span>
