---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 18fa19b4f173dd3539277e0a1c226afbee0de381
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887444"
---
# <span data-ttu-id="d11ac-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d11ac-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="d11ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d11ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d11ac-103">Cria uma nova política de backup arquivos do Azure NetApp (ANF) para uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="d11ac-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="d11ac-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d11ac-104">SYNTAX</span></span>

### <span data-ttu-id="d11ac-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d11ac-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d11ac-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d11ac-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d11ac-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d11ac-107">DESCRIPTION</span></span>
<span data-ttu-id="d11ac-108">O cmdlet **New-AzNetAppFilesActiveDirectory** cria uma nova política de backup para uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="d11ac-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="d11ac-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d11ac-109">EXAMPLES</span></span>

### <span data-ttu-id="d11ac-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d11ac-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="d11ac-111">Este comando cria a nova política de backup ANF para a conta ANF denominada "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="d11ac-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="d11ac-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d11ac-112">PARAMETERS</span></span>

### <span data-ttu-id="d11ac-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d11ac-113">-AccountName</span></span>
<span data-ttu-id="d11ac-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="d11ac-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="d11ac-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="d11ac-115">-AccountObject</span></span>
<span data-ttu-id="d11ac-116">O objeto Account da nova Política de Backup</span><span class="sxs-lookup"><span data-stu-id="d11ac-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="d11ac-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="d11ac-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="d11ac-118">Contagem de backups diários a ser manter</span><span class="sxs-lookup"><span data-stu-id="d11ac-118">Daily backups count to keep</span></span>

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

### <span data-ttu-id="d11ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11ac-119">-DefaultProfile</span></span>
<span data-ttu-id="d11ac-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d11ac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d11ac-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="d11ac-121">-Enabled</span></span>
<span data-ttu-id="d11ac-122">A propriedade para decidir a política está habilitada ou não</span><span class="sxs-lookup"><span data-stu-id="d11ac-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="d11ac-123">-Location</span><span class="sxs-lookup"><span data-stu-id="d11ac-123">-Location</span></span>
<span data-ttu-id="d11ac-124">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="d11ac-124">The location of the resource</span></span>

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

### <span data-ttu-id="d11ac-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="d11ac-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="d11ac-126">Contagem mensal de backups a ser manter</span><span class="sxs-lookup"><span data-stu-id="d11ac-126">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="d11ac-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d11ac-127">-Name</span></span>
<span data-ttu-id="d11ac-128">O nome da política de backup da ANF</span><span class="sxs-lookup"><span data-stu-id="d11ac-128">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d11ac-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d11ac-129">-ResourceGroupName</span></span>
<span data-ttu-id="d11ac-130">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="d11ac-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d11ac-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="d11ac-131">-Tag</span></span>
<span data-ttu-id="d11ac-132">Uma matriz hashtable que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="d11ac-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="d11ac-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="d11ac-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="d11ac-134">Contagem de backups semanais para manter</span><span class="sxs-lookup"><span data-stu-id="d11ac-134">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="d11ac-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="d11ac-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="d11ac-136">Contagem anual de backups a ser manter</span><span class="sxs-lookup"><span data-stu-id="d11ac-136">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="d11ac-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d11ac-137">-Confirm</span></span>
<span data-ttu-id="d11ac-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d11ac-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d11ac-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d11ac-139">-WhatIf</span></span>
<span data-ttu-id="d11ac-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d11ac-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d11ac-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d11ac-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d11ac-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11ac-142">CommonParameters</span></span>
<span data-ttu-id="d11ac-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d11ac-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11ac-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d11ac-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11ac-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d11ac-145">INPUTS</span></span>

### <span data-ttu-id="d11ac-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d11ac-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d11ac-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d11ac-147">OUTPUTS</span></span>

### <span data-ttu-id="d11ac-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d11ac-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="d11ac-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="d11ac-149">NOTES</span></span>

## <span data-ttu-id="d11ac-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d11ac-150">RELATED LINKS</span></span>
