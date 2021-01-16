---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: 34b4e43dcd09df600c73a6dd0a459a41b491da3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262606"
---
# <span data-ttu-id="307d4-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="307d4-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="307d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="307d4-102">SYNOPSIS</span></span>
<span data-ttu-id="307d4-103">Exclui um backup do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="307d4-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="307d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="307d4-104">SYNTAX</span></span>

### <span data-ttu-id="307d4-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="307d4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="307d4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="307d4-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="307d4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="307d4-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="307d4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="307d4-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="307d4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="307d4-109">DESCRIPTION</span></span>
<span data-ttu-id="307d4-110">O cmdlet **Remove-AzNetAppFilesBackup** exclui uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="307d4-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="307d4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="307d4-111">EXAMPLES</span></span>

### <span data-ttu-id="307d4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="307d4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="307d4-113">Esse comando exclui o novo ANF backup com um nome "MyBackup" para volume "myvolume".</span><span class="sxs-lookup"><span data-stu-id="307d4-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="307d4-114">OS</span><span class="sxs-lookup"><span data-stu-id="307d4-114">PARAMETERS</span></span>

### <span data-ttu-id="307d4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="307d4-115">-AccountName</span></span>
<span data-ttu-id="307d4-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="307d4-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="307d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307d4-117">-DefaultProfile</span></span>
<span data-ttu-id="307d4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="307d4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="307d4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="307d4-119">-InputObject</span></span>
<span data-ttu-id="307d4-120">O objeto de instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="307d4-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="307d4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="307d4-121">-Name</span></span>
<span data-ttu-id="307d4-122">O nome do backup do ANF</span><span class="sxs-lookup"><span data-stu-id="307d4-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="307d4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="307d4-123">-PassThru</span></span>
<span data-ttu-id="307d4-124">Retornar se o backup especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="307d4-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="307d4-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="307d4-125">-PoolName</span></span>
<span data-ttu-id="307d4-126">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="307d4-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="307d4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="307d4-127">-ResourceGroupName</span></span>
<span data-ttu-id="307d4-128">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="307d4-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="307d4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="307d4-129">-ResourceId</span></span>
<span data-ttu-id="307d4-130">A ID do recurso do backup do ANF</span><span class="sxs-lookup"><span data-stu-id="307d4-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="307d4-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="307d4-131">-VolumeName</span></span>
<span data-ttu-id="307d4-132">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="307d4-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="307d4-133">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="307d4-133">-VolumeObject</span></span>
<span data-ttu-id="307d4-134">O objeto de volume que contém o backup a ser retornado</span><span class="sxs-lookup"><span data-stu-id="307d4-134">The volume object containing the backup to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="307d4-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="307d4-135">-Confirm</span></span>
<span data-ttu-id="307d4-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="307d4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="307d4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="307d4-137">-WhatIf</span></span>
<span data-ttu-id="307d4-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="307d4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="307d4-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="307d4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="307d4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307d4-140">CommonParameters</span></span>
<span data-ttu-id="307d4-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="307d4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307d4-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="307d4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307d4-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="307d4-143">INPUTS</span></span>

### <span data-ttu-id="307d4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="307d4-144">System.String</span></span>

### <span data-ttu-id="307d4-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="307d4-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="307d4-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="307d4-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="307d4-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="307d4-147">OUTPUTS</span></span>

### <span data-ttu-id="307d4-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="307d4-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="307d4-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="307d4-149">NOTES</span></span>

## <span data-ttu-id="307d4-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="307d4-150">RELATED LINKS</span></span>
