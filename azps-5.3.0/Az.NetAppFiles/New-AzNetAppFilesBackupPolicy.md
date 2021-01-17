---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427049"
---
# <span data-ttu-id="df9d0-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="df9d0-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="df9d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="df9d0-103">Cria uma nova política de backup do Azure NetApp Files (ANF) para uma conta do ANF.</span><span class="sxs-lookup"><span data-stu-id="df9d0-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="df9d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df9d0-104">SYNTAX</span></span>

### <span data-ttu-id="df9d0-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="df9d0-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df9d0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df9d0-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df9d0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df9d0-107">DESCRIPTION</span></span>
<span data-ttu-id="df9d0-108">O cmdlet **New-AzNetAppFilesActiveDirectory** cria uma nova política de backup para uma conta do ANF.</span><span class="sxs-lookup"><span data-stu-id="df9d0-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="df9d0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df9d0-109">EXAMPLES</span></span>

### <span data-ttu-id="df9d0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df9d0-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="df9d0-111">Esse comando cria a nova política de backup do ANF para ANF conta denominada "minha conta".</span><span class="sxs-lookup"><span data-stu-id="df9d0-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="df9d0-112">OS</span><span class="sxs-lookup"><span data-stu-id="df9d0-112">PARAMETERS</span></span>

### <span data-ttu-id="df9d0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df9d0-113">-AccountName</span></span>
<span data-ttu-id="df9d0-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="df9d0-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="df9d0-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="df9d0-115">-AccountObject</span></span>
<span data-ttu-id="df9d0-116">O objeto de conta para a nova política de backup</span><span class="sxs-lookup"><span data-stu-id="df9d0-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="df9d0-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="df9d0-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="df9d0-118">Contagem de backups diários a ser mantida</span><span class="sxs-lookup"><span data-stu-id="df9d0-118">Daily backups count to keep</span></span>

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

### <span data-ttu-id="df9d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9d0-119">-DefaultProfile</span></span>
<span data-ttu-id="df9d0-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df9d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df9d0-121">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="df9d0-121">-Enabled</span></span>
<span data-ttu-id="df9d0-122">A propriedade para decidir se política está habilitada ou não</span><span class="sxs-lookup"><span data-stu-id="df9d0-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="df9d0-123">-Local</span><span class="sxs-lookup"><span data-stu-id="df9d0-123">-Location</span></span>
<span data-ttu-id="df9d0-124">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="df9d0-124">The location of the resource</span></span>

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

### <span data-ttu-id="df9d0-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="df9d0-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="df9d0-126">Contagem de backups mensais a ser mantida</span><span class="sxs-lookup"><span data-stu-id="df9d0-126">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="df9d0-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="df9d0-127">-Name</span></span>
<span data-ttu-id="df9d0-128">O nome da política de backup do ANF</span><span class="sxs-lookup"><span data-stu-id="df9d0-128">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="df9d0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df9d0-129">-ResourceGroupName</span></span>
<span data-ttu-id="df9d0-130">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="df9d0-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="df9d0-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="df9d0-131">-Tag</span></span>
<span data-ttu-id="df9d0-132">Uma matriz de Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="df9d0-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="df9d0-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="df9d0-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="df9d0-134">Contagem semanal de backups a ser mantida</span><span class="sxs-lookup"><span data-stu-id="df9d0-134">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="df9d0-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="df9d0-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="df9d0-136">Contagem de backups anuais para manter</span><span class="sxs-lookup"><span data-stu-id="df9d0-136">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="df9d0-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df9d0-137">-Confirm</span></span>
<span data-ttu-id="df9d0-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df9d0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df9d0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df9d0-139">-WhatIf</span></span>
<span data-ttu-id="df9d0-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df9d0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df9d0-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df9d0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df9d0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9d0-142">CommonParameters</span></span>
<span data-ttu-id="df9d0-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df9d0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9d0-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df9d0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9d0-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df9d0-145">INPUTS</span></span>

### <span data-ttu-id="df9d0-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="df9d0-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="df9d0-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df9d0-147">OUTPUTS</span></span>

### <span data-ttu-id="df9d0-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="df9d0-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="df9d0-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df9d0-149">NOTES</span></span>

## <span data-ttu-id="df9d0-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df9d0-150">RELATED LINKS</span></span>
