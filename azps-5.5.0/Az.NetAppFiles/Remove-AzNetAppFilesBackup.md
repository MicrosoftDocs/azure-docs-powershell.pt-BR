---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: 34b4e43dcd09df600c73a6dd0a459a41b491da3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114730"
---
# <span data-ttu-id="f8b26-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="f8b26-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="f8b26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8b26-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b26-103">Exclui um backup do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="f8b26-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="f8b26-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8b26-104">SYNTAX</span></span>

### <span data-ttu-id="f8b26-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f8b26-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8b26-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8b26-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8b26-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8b26-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8b26-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8b26-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8b26-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8b26-109">DESCRIPTION</span></span>
<span data-ttu-id="f8b26-110">O **cmdlet Remove-AzNetAppFilesBackup** exclui uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="f8b26-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="f8b26-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f8b26-111">EXAMPLES</span></span>

### <span data-ttu-id="f8b26-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8b26-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="f8b26-113">Esse comando exclui o novo backup da ANF com o nome "MyBackup" para volume "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="f8b26-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="f8b26-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8b26-114">PARAMETERS</span></span>

### <span data-ttu-id="f8b26-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="f8b26-115">-AccountName</span></span>
<span data-ttu-id="f8b26-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="f8b26-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f8b26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b26-117">-DefaultProfile</span></span>
<span data-ttu-id="f8b26-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b26-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8b26-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8b26-119">-InputObject</span></span>
<span data-ttu-id="f8b26-120">O objeto instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="f8b26-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="f8b26-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8b26-121">-Name</span></span>
<span data-ttu-id="f8b26-122">O nome do backup da ANF</span><span class="sxs-lookup"><span data-stu-id="f8b26-122">The name of the ANF backup</span></span>

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

### <span data-ttu-id="f8b26-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8b26-123">-PassThru</span></span>
<span data-ttu-id="f8b26-124">Retornar se o backup especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="f8b26-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="f8b26-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f8b26-125">-PoolName</span></span>
<span data-ttu-id="f8b26-126">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="f8b26-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f8b26-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b26-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8b26-128">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="f8b26-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f8b26-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8b26-129">-ResourceId</span></span>
<span data-ttu-id="f8b26-130">A ID do recurso do Backup ANF</span><span class="sxs-lookup"><span data-stu-id="f8b26-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="f8b26-131">-Nomedo Volume</span><span class="sxs-lookup"><span data-stu-id="f8b26-131">-VolumeName</span></span>
<span data-ttu-id="f8b26-132">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="f8b26-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="f8b26-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="f8b26-133">-VolumeObject</span></span>
<span data-ttu-id="f8b26-134">O objeto de volume que contém o backup a ser retornado</span><span class="sxs-lookup"><span data-stu-id="f8b26-134">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="f8b26-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f8b26-135">-Confirm</span></span>
<span data-ttu-id="f8b26-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8b26-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8b26-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8b26-137">-WhatIf</span></span>
<span data-ttu-id="f8b26-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f8b26-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8b26-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f8b26-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8b26-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b26-140">CommonParameters</span></span>
<span data-ttu-id="f8b26-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b26-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b26-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8b26-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b26-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="f8b26-143">INPUTS</span></span>

### <span data-ttu-id="f8b26-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f8b26-144">System.String</span></span>

### <span data-ttu-id="f8b26-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f8b26-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="f8b26-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="f8b26-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="f8b26-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="f8b26-147">OUTPUTS</span></span>

### <span data-ttu-id="f8b26-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f8b26-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f8b26-149">Notas</span><span class="sxs-lookup"><span data-stu-id="f8b26-149">NOTES</span></span>

## <span data-ttu-id="f8b26-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8b26-150">RELATED LINKS</span></span>
