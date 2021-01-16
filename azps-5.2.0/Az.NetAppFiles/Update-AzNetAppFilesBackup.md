---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: a2cab03bb88d5b642a95142030eb646b2a5abef4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258594"
---
# <span data-ttu-id="9c5cb-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="9c5cb-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="9c5cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5cb-103">Atualiza um backup do Azure NetApp Files (ANF) para os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="9c5cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c5cb-104">SYNTAX</span></span>

### <span data-ttu-id="9c5cb-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c5cb-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c5cb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c5cb-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c5cb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c5cb-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c5cb-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c5cb-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c5cb-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c5cb-109">DESCRIPTION</span></span>
<span data-ttu-id="9c5cb-110">O cmdlet **Update-AzNetAppFilesBackup** modifica um backup do ANF.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="9c5cb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c5cb-111">EXAMPLES</span></span>

### <span data-ttu-id="9c5cb-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c5cb-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="9c5cb-113">Esse comando executa uma atualização no backup fornecido modificando o nome de usuário para o fornecido.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="9c5cb-114">OS</span><span class="sxs-lookup"><span data-stu-id="9c5cb-114">PARAMETERS</span></span>

### <span data-ttu-id="9c5cb-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c5cb-115">-AccountName</span></span>
<span data-ttu-id="9c5cb-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="9c5cb-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9c5cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5cb-117">-DefaultProfile</span></span>
<span data-ttu-id="9c5cb-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c5cb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c5cb-119">-InputObject</span></span>
<span data-ttu-id="9c5cb-120">O objeto de instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="9c5cb-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="9c5cb-121">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="9c5cb-121">-Label</span></span>
<span data-ttu-id="9c5cb-122">Rótulo para backup</span><span class="sxs-lookup"><span data-stu-id="9c5cb-122">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5cb-123">-Local</span><span class="sxs-lookup"><span data-stu-id="9c5cb-123">-Location</span></span>
<span data-ttu-id="9c5cb-124">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="9c5cb-124">The location of the resource</span></span>

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

### <span data-ttu-id="9c5cb-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c5cb-125">-Name</span></span>
<span data-ttu-id="9c5cb-126">O nome da política de backup do ANF</span><span class="sxs-lookup"><span data-stu-id="9c5cb-126">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5cb-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9c5cb-127">-PoolName</span></span>
<span data-ttu-id="9c5cb-128">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="9c5cb-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="9c5cb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c5cb-129">-ResourceGroupName</span></span>
<span data-ttu-id="9c5cb-130">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="9c5cb-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9c5cb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c5cb-131">-ResourceId</span></span>
<span data-ttu-id="9c5cb-132">A ID do recurso do backup do ANF</span><span class="sxs-lookup"><span data-stu-id="9c5cb-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="9c5cb-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="9c5cb-133">-Tag</span></span>
<span data-ttu-id="9c5cb-134">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="9c5cb-134">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5cb-135">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="9c5cb-135">-VolumeName</span></span>
<span data-ttu-id="9c5cb-136">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="9c5cb-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="9c5cb-137">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="9c5cb-137">-VolumeObject</span></span>
<span data-ttu-id="9c5cb-138">O objeto de volume que contém o backup a ser retornado</span><span class="sxs-lookup"><span data-stu-id="9c5cb-138">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="9c5cb-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c5cb-139">-Confirm</span></span>
<span data-ttu-id="9c5cb-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c5cb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c5cb-141">-WhatIf</span></span>
<span data-ttu-id="9c5cb-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c5cb-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c5cb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5cb-144">CommonParameters</span></span>
<span data-ttu-id="9c5cb-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5cb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5cb-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c5cb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5cb-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c5cb-147">INPUTS</span></span>

### <span data-ttu-id="9c5cb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9c5cb-148">System.String</span></span>

### <span data-ttu-id="9c5cb-149">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9c5cb-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="9c5cb-150">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="9c5cb-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="9c5cb-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c5cb-151">OUTPUTS</span></span>

### <span data-ttu-id="9c5cb-152">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9c5cb-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="9c5cb-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c5cb-153">NOTES</span></span>

## <span data-ttu-id="9c5cb-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c5cb-154">RELATED LINKS</span></span>
