---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117496"
---
# <span data-ttu-id="3e0dc-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3e0dc-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="3e0dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e0dc-102">SYNOPSIS</span></span>
<span data-ttu-id="3e0dc-103">Cria uma nova política de backup Azure NetApp Files (ANF) para uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="3e0dc-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="3e0dc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e0dc-104">SYNTAX</span></span>

### <span data-ttu-id="3e0dc-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3e0dc-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e0dc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e0dc-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e0dc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e0dc-107">DESCRIPTION</span></span>
<span data-ttu-id="3e0dc-108">O cmdlet **New-AzNetAppFilesActiveDirectory cria** uma nova política de backup para uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="3e0dc-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="3e0dc-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e0dc-109">EXAMPLES</span></span>

### <span data-ttu-id="3e0dc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e0dc-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="3e0dc-111">Esse comando cria a nova política de backup ANF para a conta ANF chamada conta "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="3e0dc-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="3e0dc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e0dc-112">PARAMETERS</span></span>

### <span data-ttu-id="3e0dc-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="3e0dc-113">-AccountName</span></span>
<span data-ttu-id="3e0dc-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="3e0dc-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="3e0dc-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="3e0dc-115">-AccountObject</span></span>
<span data-ttu-id="3e0dc-116">O objeto Conta da nova Política de Backup</span><span class="sxs-lookup"><span data-stu-id="3e0dc-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="3e0dc-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="3e0dc-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="3e0dc-118">Os backups diários contam para manter</span><span class="sxs-lookup"><span data-stu-id="3e0dc-118">Daily backups count to keep</span></span>

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

### <span data-ttu-id="3e0dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e0dc-119">-DefaultProfile</span></span>
<span data-ttu-id="3e0dc-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e0dc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e0dc-121">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="3e0dc-121">-Enabled</span></span>
<span data-ttu-id="3e0dc-122">A propriedade para decidir a política está habilitada ou não</span><span class="sxs-lookup"><span data-stu-id="3e0dc-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="3e0dc-123">-Local</span><span class="sxs-lookup"><span data-stu-id="3e0dc-123">-Location</span></span>
<span data-ttu-id="3e0dc-124">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="3e0dc-124">The location of the resource</span></span>

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

### <span data-ttu-id="3e0dc-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="3e0dc-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="3e0dc-126">Contagem mensal de backups a ser manter</span><span class="sxs-lookup"><span data-stu-id="3e0dc-126">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="3e0dc-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e0dc-127">-Name</span></span>
<span data-ttu-id="3e0dc-128">O nome da política de backup da ANF</span><span class="sxs-lookup"><span data-stu-id="3e0dc-128">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="3e0dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e0dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="3e0dc-130">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="3e0dc-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="3e0dc-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="3e0dc-131">-Tag</span></span>
<span data-ttu-id="3e0dc-132">Uma matriz de tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="3e0dc-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="3e0dc-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="3e0dc-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="3e0dc-134">Os backups semanais contam para manter</span><span class="sxs-lookup"><span data-stu-id="3e0dc-134">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="3e0dc-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="3e0dc-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="3e0dc-136">A contagem anual de backups deve ser guardada</span><span class="sxs-lookup"><span data-stu-id="3e0dc-136">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="3e0dc-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3e0dc-137">-Confirm</span></span>
<span data-ttu-id="3e0dc-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e0dc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e0dc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e0dc-139">-WhatIf</span></span>
<span data-ttu-id="3e0dc-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3e0dc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e0dc-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e0dc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e0dc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e0dc-142">CommonParameters</span></span>
<span data-ttu-id="3e0dc-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e0dc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e0dc-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e0dc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e0dc-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e0dc-145">INPUTS</span></span>

### <span data-ttu-id="3e0dc-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3e0dc-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="3e0dc-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e0dc-147">OUTPUTS</span></span>

### <span data-ttu-id="3e0dc-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3e0dc-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="3e0dc-149">Notas</span><span class="sxs-lookup"><span data-stu-id="3e0dc-149">NOTES</span></span>

## <span data-ttu-id="3e0dc-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e0dc-150">RELATED LINKS</span></span>
