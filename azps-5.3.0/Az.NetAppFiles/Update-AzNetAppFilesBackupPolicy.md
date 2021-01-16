---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 0cebe34948984e36c9ad2fbe30de8da3a0e0ca92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271933"
---
# <span data-ttu-id="def77-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="def77-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="def77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="def77-102">SYNOPSIS</span></span>
<span data-ttu-id="def77-103">Atualiza uma política de backup de arquivos do Azure NetApp (ANF) para os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="def77-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="def77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="def77-104">SYNTAX</span></span>

### <span data-ttu-id="def77-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="def77-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="def77-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="def77-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="def77-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="def77-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="def77-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="def77-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="def77-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="def77-109">DESCRIPTION</span></span>
<span data-ttu-id="def77-110">O cmdlet **Update-AzNetAppFilesBackupPolicy** modifica uma política de backup do ANF.</span><span class="sxs-lookup"><span data-stu-id="def77-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="def77-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="def77-111">EXAMPLES</span></span>

### <span data-ttu-id="def77-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="def77-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="def77-113">Esse comando altera a política de backup do ANF "MyBackupPolicy" para ter o DailyBackupsToKeep especificado.</span><span class="sxs-lookup"><span data-stu-id="def77-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="def77-114">OS</span><span class="sxs-lookup"><span data-stu-id="def77-114">PARAMETERS</span></span>

### <span data-ttu-id="def77-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="def77-115">-AccountName</span></span>
<span data-ttu-id="def77-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="def77-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="def77-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="def77-117">-AccountObject</span></span>
<span data-ttu-id="def77-118">O objeto de conta que contém a política de backup a ser atualizada</span><span class="sxs-lookup"><span data-stu-id="def77-118">The Account object containing the Backup Policy to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="def77-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="def77-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="def77-120">Contagem de backups diários a ser mantida</span><span class="sxs-lookup"><span data-stu-id="def77-120">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def77-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def77-121">-DefaultProfile</span></span>
<span data-ttu-id="def77-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="def77-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="def77-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="def77-123">-InputObject</span></span>
<span data-ttu-id="def77-124">O objeto BackupPolicy para remover</span><span class="sxs-lookup"><span data-stu-id="def77-124">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="def77-125">-Local</span><span class="sxs-lookup"><span data-stu-id="def77-125">-Location</span></span>
<span data-ttu-id="def77-126">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="def77-126">The location of the resource</span></span>

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

### <span data-ttu-id="def77-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="def77-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="def77-128">Contagem de backups mensais a ser mantida</span><span class="sxs-lookup"><span data-stu-id="def77-128">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def77-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="def77-129">-Name</span></span>
<span data-ttu-id="def77-130">O nome da política de backup do ANF</span><span class="sxs-lookup"><span data-stu-id="def77-130">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="def77-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="def77-131">-ResourceGroupName</span></span>
<span data-ttu-id="def77-132">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="def77-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="def77-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="def77-133">-ResourceId</span></span>
<span data-ttu-id="def77-134">A ID do recurso da política de backup do ANF</span><span class="sxs-lookup"><span data-stu-id="def77-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="def77-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="def77-135">-Tag</span></span>
<span data-ttu-id="def77-136">Uma matriz de Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="def77-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="def77-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="def77-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="def77-138">Contagem semanal de backups a ser mantida</span><span class="sxs-lookup"><span data-stu-id="def77-138">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def77-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="def77-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="def77-140">Contagem de backups anuais para manter</span><span class="sxs-lookup"><span data-stu-id="def77-140">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def77-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="def77-141">-Confirm</span></span>
<span data-ttu-id="def77-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="def77-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="def77-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="def77-143">-WhatIf</span></span>
<span data-ttu-id="def77-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="def77-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="def77-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="def77-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="def77-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def77-146">CommonParameters</span></span>
<span data-ttu-id="def77-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def77-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def77-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="def77-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def77-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="def77-149">INPUTS</span></span>

### <span data-ttu-id="def77-150">System. String</span><span class="sxs-lookup"><span data-stu-id="def77-150">System.String</span></span>

### <span data-ttu-id="def77-151">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="def77-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="def77-152">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="def77-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="def77-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="def77-153">OUTPUTS</span></span>

### <span data-ttu-id="def77-154">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="def77-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="def77-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="def77-155">NOTES</span></span>

## <span data-ttu-id="def77-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="def77-156">RELATED LINKS</span></span>
