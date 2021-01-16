---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 6606de1a5d4de6df6ecafa700ac1b93d31399b43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271944"
---
# <span data-ttu-id="0c296-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="0c296-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="0c296-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c296-102">SYNOPSIS</span></span>
<span data-ttu-id="0c296-103">Restaurar/reverter um volume para um de seus instantâneos</span><span class="sxs-lookup"><span data-stu-id="0c296-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="0c296-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c296-104">SYNTAX</span></span>

### <span data-ttu-id="0c296-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0c296-105">ByFieldsParameterSet (Default)</span></span>
```
Restore-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c296-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c296-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c296-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c296-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c296-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c296-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c296-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c296-109">DESCRIPTION</span></span>
<span data-ttu-id="0c296-110">Restaurar/reverter um volume para o instantâneo especificado no parâmetro Instantâneoid</span><span class="sxs-lookup"><span data-stu-id="0c296-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="0c296-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c296-111">EXAMPLES</span></span>

### <span data-ttu-id="0c296-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c296-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="0c296-113">Esse comando restaura/reverte o volume myvolume para um de seus instantâneos com a captura de tela do 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="0c296-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="0c296-114">OS</span><span class="sxs-lookup"><span data-stu-id="0c296-114">PARAMETERS</span></span>

### <span data-ttu-id="0c296-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c296-115">-AccountName</span></span>
<span data-ttu-id="0c296-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="0c296-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="0c296-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c296-117">-DefaultProfile</span></span>
<span data-ttu-id="0c296-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c296-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c296-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c296-119">-InputObject</span></span>
<span data-ttu-id="0c296-120">O objeto volume a ser removido</span><span class="sxs-lookup"><span data-stu-id="0c296-120">The volume object to remove</span></span>

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

### <span data-ttu-id="0c296-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c296-121">-Name</span></span>
<span data-ttu-id="0c296-122">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="0c296-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c296-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c296-123">-PassThru</span></span>
<span data-ttu-id="0c296-124">Retornar se o volume especificado foi restaurado/revertido com êxito</span><span class="sxs-lookup"><span data-stu-id="0c296-124">Return whether the specified volume was successfully restored/reverted</span></span>

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

### <span data-ttu-id="0c296-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="0c296-125">-PoolName</span></span>
<span data-ttu-id="0c296-126">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="0c296-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="0c296-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="0c296-127">-PoolObject</span></span>
<span data-ttu-id="0c296-128">O objeto de pool que contém o volume a ser removido</span><span class="sxs-lookup"><span data-stu-id="0c296-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c296-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c296-129">-ResourceGroupName</span></span>
<span data-ttu-id="0c296-130">O grupo de recursos do volume ANF</span><span class="sxs-lookup"><span data-stu-id="0c296-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="0c296-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c296-131">-ResourceId</span></span>
<span data-ttu-id="0c296-132">A ID do recurso do volume ANF</span><span class="sxs-lookup"><span data-stu-id="0c296-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="0c296-133">-Captura de imagem</span><span class="sxs-lookup"><span data-stu-id="0c296-133">-SnapshotId</span></span>
<span data-ttu-id="0c296-134">Instantâneoid do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="0c296-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="0c296-135">UUID v4 usado para identificar o instantâneo</span><span class="sxs-lookup"><span data-stu-id="0c296-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c296-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0c296-136">-Confirm</span></span>
<span data-ttu-id="0c296-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c296-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c296-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c296-138">-WhatIf</span></span>
<span data-ttu-id="0c296-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c296-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c296-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c296-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c296-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c296-141">CommonParameters</span></span>
<span data-ttu-id="0c296-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c296-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c296-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c296-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c296-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c296-144">INPUTS</span></span>

### <span data-ttu-id="0c296-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0c296-145">System.String</span></span>

### <span data-ttu-id="0c296-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0c296-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="0c296-147">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="0c296-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="0c296-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c296-148">OUTPUTS</span></span>

### <span data-ttu-id="0c296-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c296-149">System.Boolean</span></span>

## <span data-ttu-id="0c296-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c296-150">NOTES</span></span>

## <span data-ttu-id="0c296-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c296-151">RELATED LINKS</span></span>
