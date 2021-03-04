---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 14c2a58c40aa29f1b48902be5d82911f70a71cd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887401"
---
# <span data-ttu-id="55937-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="55937-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="55937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55937-102">SYNOPSIS</span></span>
<span data-ttu-id="55937-103">Atualiza uma política de backup arquivos do Azure NetApp (ANF) para os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="55937-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="55937-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="55937-104">SYNTAX</span></span>

### <span data-ttu-id="55937-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="55937-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55937-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55937-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55937-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55937-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55937-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55937-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55937-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="55937-109">DESCRIPTION</span></span>
<span data-ttu-id="55937-110">O cmdlet **Update-AzNetAppFilesBackupPolicy** modifica uma política de backup ANF.</span><span class="sxs-lookup"><span data-stu-id="55937-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="55937-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55937-111">EXAMPLES</span></span>

### <span data-ttu-id="55937-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55937-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="55937-113">Este comando altera a política de backup da ANF "MyBackupPolicy" para ter o DailyBackupsToKeep determinado.</span><span class="sxs-lookup"><span data-stu-id="55937-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="55937-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="55937-114">PARAMETERS</span></span>

### <span data-ttu-id="55937-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55937-115">-AccountName</span></span>
<span data-ttu-id="55937-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="55937-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="55937-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="55937-117">-AccountObject</span></span>
<span data-ttu-id="55937-118">O objeto Account que contém a Política de Backup a ser atualizada</span><span class="sxs-lookup"><span data-stu-id="55937-118">The Account object containing the Backup Policy to update</span></span>

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

### <span data-ttu-id="55937-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="55937-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="55937-120">Contagem de backups diários a ser manter</span><span class="sxs-lookup"><span data-stu-id="55937-120">Daily backups count to keep</span></span>

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

### <span data-ttu-id="55937-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55937-121">-DefaultProfile</span></span>
<span data-ttu-id="55937-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55937-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55937-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55937-123">-InputObject</span></span>
<span data-ttu-id="55937-124">O objeto BackupPolicy a ser removido</span><span class="sxs-lookup"><span data-stu-id="55937-124">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="55937-125">-Location</span><span class="sxs-lookup"><span data-stu-id="55937-125">-Location</span></span>
<span data-ttu-id="55937-126">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="55937-126">The location of the resource</span></span>

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

### <span data-ttu-id="55937-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="55937-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="55937-128">Contagem mensal de backups a ser manter</span><span class="sxs-lookup"><span data-stu-id="55937-128">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="55937-129">-Name</span><span class="sxs-lookup"><span data-stu-id="55937-129">-Name</span></span>
<span data-ttu-id="55937-130">O nome da política de backup da ANF</span><span class="sxs-lookup"><span data-stu-id="55937-130">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="55937-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55937-131">-ResourceGroupName</span></span>
<span data-ttu-id="55937-132">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="55937-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="55937-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55937-133">-ResourceId</span></span>
<span data-ttu-id="55937-134">A id de recurso da Política de Backup da ANF</span><span class="sxs-lookup"><span data-stu-id="55937-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="55937-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="55937-135">-Tag</span></span>
<span data-ttu-id="55937-136">Uma matriz hashtable que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="55937-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="55937-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="55937-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="55937-138">Contagem de backups semanais para manter</span><span class="sxs-lookup"><span data-stu-id="55937-138">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="55937-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="55937-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="55937-140">Contagem anual de backups a ser manter</span><span class="sxs-lookup"><span data-stu-id="55937-140">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="55937-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55937-141">-Confirm</span></span>
<span data-ttu-id="55937-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55937-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55937-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55937-143">-WhatIf</span></span>
<span data-ttu-id="55937-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55937-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55937-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55937-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55937-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55937-146">CommonParameters</span></span>
<span data-ttu-id="55937-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55937-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55937-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55937-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55937-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55937-149">INPUTS</span></span>

### <span data-ttu-id="55937-150">System.String</span><span class="sxs-lookup"><span data-stu-id="55937-150">System.String</span></span>

### <span data-ttu-id="55937-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="55937-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="55937-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="55937-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="55937-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="55937-153">OUTPUTS</span></span>

### <span data-ttu-id="55937-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="55937-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="55937-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="55937-155">NOTES</span></span>

## <span data-ttu-id="55937-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55937-156">RELATED LINKS</span></span>
