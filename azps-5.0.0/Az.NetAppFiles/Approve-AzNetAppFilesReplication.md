---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118392"
---
# <span data-ttu-id="de9db-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="de9db-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="de9db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de9db-102">SYNOPSIS</span></span>
<span data-ttu-id="de9db-103">Aprovar/autorizar a conexão de replicação no volume de origem</span><span class="sxs-lookup"><span data-stu-id="de9db-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="de9db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de9db-104">SYNTAX</span></span>

### <span data-ttu-id="de9db-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="de9db-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de9db-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de9db-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de9db-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de9db-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de9db-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de9db-108">DESCRIPTION</span></span>
<span data-ttu-id="de9db-109">Aprovar a conexão de replicação no volume de origem</span><span class="sxs-lookup"><span data-stu-id="de9db-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="de9db-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de9db-110">EXAMPLES</span></span>

### <span data-ttu-id="de9db-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de9db-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="de9db-112">Esse comando aprova a replicação no MyAnfVolume.</span><span class="sxs-lookup"><span data-stu-id="de9db-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="de9db-113">OS</span><span class="sxs-lookup"><span data-stu-id="de9db-113">PARAMETERS</span></span>

### <span data-ttu-id="de9db-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="de9db-114">-AccountName</span></span>
<span data-ttu-id="de9db-115">O nome da conta ANF do volume de origem de replicação</span><span class="sxs-lookup"><span data-stu-id="de9db-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="de9db-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="de9db-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="de9db-117">A ID do sistema de arquivos do volume de proteção de dados de destino</span><span class="sxs-lookup"><span data-stu-id="de9db-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="de9db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de9db-118">-DefaultProfile</span></span>
<span data-ttu-id="de9db-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de9db-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de9db-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de9db-120">-InputObject</span></span>
<span data-ttu-id="de9db-121">O objeto de volume de origem ANF para autorizar o destino de replicação</span><span class="sxs-lookup"><span data-stu-id="de9db-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="de9db-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="de9db-122">-Name</span></span>
<span data-ttu-id="de9db-123">O nome do volume de origem de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="de9db-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="de9db-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de9db-124">-PassThru</span></span>
<span data-ttu-id="de9db-125">Retornar se a autorização de replicação do volume especificado foi realizada</span><span class="sxs-lookup"><span data-stu-id="de9db-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="de9db-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="de9db-126">-PoolName</span></span>
<span data-ttu-id="de9db-127">O nome do pool ANF do volume de origem de replicação</span><span class="sxs-lookup"><span data-stu-id="de9db-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="de9db-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de9db-128">-ResourceGroupName</span></span>
<span data-ttu-id="de9db-129">O grupo de recursos do volume de origem de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="de9db-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="de9db-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de9db-130">-ResourceId</span></span>
<span data-ttu-id="de9db-131">A ID do recurso do volume de origem de replicação do ANF</span><span class="sxs-lookup"><span data-stu-id="de9db-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="de9db-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="de9db-132">-Confirm</span></span>
<span data-ttu-id="de9db-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de9db-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de9db-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de9db-134">-WhatIf</span></span>
<span data-ttu-id="de9db-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de9db-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de9db-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de9db-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de9db-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de9db-137">CommonParameters</span></span>
<span data-ttu-id="de9db-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de9db-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de9db-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de9db-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de9db-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de9db-140">INPUTS</span></span>

### <span data-ttu-id="de9db-141">System. String</span><span class="sxs-lookup"><span data-stu-id="de9db-141">System.String</span></span>

### <span data-ttu-id="de9db-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="de9db-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="de9db-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de9db-143">OUTPUTS</span></span>

### <span data-ttu-id="de9db-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de9db-144">System.Boolean</span></span>

## <span data-ttu-id="de9db-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de9db-145">NOTES</span></span>

## <span data-ttu-id="de9db-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de9db-146">RELATED LINKS</span></span>
