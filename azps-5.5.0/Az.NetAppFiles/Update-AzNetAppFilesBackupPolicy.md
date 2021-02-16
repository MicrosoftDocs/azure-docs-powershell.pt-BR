---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 0cebe34948984e36c9ad2fbe30de8da3a0e0ca92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118400"
---
# <span data-ttu-id="c8e02-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="c8e02-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="c8e02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8e02-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e02-103">Atualiza uma política de backup de Arquivos Azure NetApp (ANF) para os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="c8e02-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="c8e02-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8e02-104">SYNTAX</span></span>

### <span data-ttu-id="c8e02-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c8e02-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8e02-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8e02-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8e02-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8e02-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8e02-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8e02-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8e02-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8e02-109">DESCRIPTION</span></span>
<span data-ttu-id="c8e02-110">O cmdlet **Update-AzNetAppFilesBackupPolicy** modifica uma política de backup ANF.</span><span class="sxs-lookup"><span data-stu-id="c8e02-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="c8e02-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8e02-111">EXAMPLES</span></span>

### <span data-ttu-id="c8e02-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8e02-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="c8e02-113">Esse comando altera a política de backup "MyBackupPolicy" da ANF para que o DailyBackupsToKeep seja determinado.</span><span class="sxs-lookup"><span data-stu-id="c8e02-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="c8e02-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8e02-114">PARAMETERS</span></span>

### <span data-ttu-id="c8e02-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="c8e02-115">-AccountName</span></span>
<span data-ttu-id="c8e02-116">O nome da conta da ANF</span><span class="sxs-lookup"><span data-stu-id="c8e02-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="c8e02-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="c8e02-117">-AccountObject</span></span>
<span data-ttu-id="c8e02-118">O objeto Conta que contém a Política de Backup a ser atualizada</span><span class="sxs-lookup"><span data-stu-id="c8e02-118">The Account object containing the Backup Policy to update</span></span>

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

### <span data-ttu-id="c8e02-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="c8e02-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="c8e02-120">Os backups diários contam para manter</span><span class="sxs-lookup"><span data-stu-id="c8e02-120">Daily backups count to keep</span></span>

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

### <span data-ttu-id="c8e02-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e02-121">-DefaultProfile</span></span>
<span data-ttu-id="c8e02-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e02-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8e02-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8e02-123">-InputObject</span></span>
<span data-ttu-id="c8e02-124">O objeto BackupPolicy a ser removido</span><span class="sxs-lookup"><span data-stu-id="c8e02-124">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="c8e02-125">-Local</span><span class="sxs-lookup"><span data-stu-id="c8e02-125">-Location</span></span>
<span data-ttu-id="c8e02-126">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="c8e02-126">The location of the resource</span></span>

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

### <span data-ttu-id="c8e02-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="c8e02-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="c8e02-128">Contagem mensal de backups a ser manter</span><span class="sxs-lookup"><span data-stu-id="c8e02-128">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="c8e02-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8e02-129">-Name</span></span>
<span data-ttu-id="c8e02-130">O nome da política de backup da ANF</span><span class="sxs-lookup"><span data-stu-id="c8e02-130">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="c8e02-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e02-131">-ResourceGroupName</span></span>
<span data-ttu-id="c8e02-132">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="c8e02-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c8e02-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8e02-133">-ResourceId</span></span>
<span data-ttu-id="c8e02-134">A ID do recurso da Política de Backup da ANF</span><span class="sxs-lookup"><span data-stu-id="c8e02-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="c8e02-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8e02-135">-Tag</span></span>
<span data-ttu-id="c8e02-136">Uma matriz de tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="c8e02-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="c8e02-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="c8e02-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="c8e02-138">Os backups semanais contam para manter</span><span class="sxs-lookup"><span data-stu-id="c8e02-138">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="c8e02-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="c8e02-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="c8e02-140">A contagem anual de backups deve ser guardada</span><span class="sxs-lookup"><span data-stu-id="c8e02-140">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="c8e02-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c8e02-141">-Confirm</span></span>
<span data-ttu-id="c8e02-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8e02-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8e02-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8e02-143">-WhatIf</span></span>
<span data-ttu-id="c8e02-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c8e02-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8e02-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8e02-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8e02-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e02-146">CommonParameters</span></span>
<span data-ttu-id="c8e02-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e02-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e02-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8e02-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e02-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="c8e02-149">INPUTS</span></span>

### <span data-ttu-id="c8e02-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c8e02-150">System.String</span></span>

### <span data-ttu-id="c8e02-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c8e02-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="c8e02-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="c8e02-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="c8e02-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="c8e02-153">OUTPUTS</span></span>

### <span data-ttu-id="c8e02-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="c8e02-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="c8e02-155">Notas</span><span class="sxs-lookup"><span data-stu-id="c8e02-155">NOTES</span></span>

## <span data-ttu-id="c8e02-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8e02-156">RELATED LINKS</span></span>
