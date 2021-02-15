---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115223"
---
# <span data-ttu-id="93f13-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="93f13-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="93f13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93f13-102">SYNOPSIS</span></span>
<span data-ttu-id="93f13-103">Atualiza uma política de instantâneo do Azure NetApp Files (ANF) para os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="93f13-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="93f13-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93f13-104">SYNTAX</span></span>

### <span data-ttu-id="93f13-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="93f13-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93f13-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93f13-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93f13-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93f13-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93f13-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93f13-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93f13-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="93f13-109">DESCRIPTION</span></span>
<span data-ttu-id="93f13-110">O cmdlet **Update-AzNetAppFilesSnapshotPolicy** modifica uma política de instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="93f13-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="93f13-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="93f13-111">EXAMPLES</span></span>

### <span data-ttu-id="93f13-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="93f13-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="93f13-113">Esse comando altera a política de backup da ANF "MySnapshotPolicy" para ter o hourlySchedule determinado.</span><span class="sxs-lookup"><span data-stu-id="93f13-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="93f13-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93f13-114">PARAMETERS</span></span>

### <span data-ttu-id="93f13-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="93f13-115">-AccountName</span></span>
<span data-ttu-id="93f13-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="93f13-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="93f13-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="93f13-117">-AccountObject</span></span>
<span data-ttu-id="93f13-118">A Conta do novo objeto de Política de Instantâneo</span><span class="sxs-lookup"><span data-stu-id="93f13-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="93f13-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="93f13-119">-DailySchedule</span></span>
<span data-ttu-id="93f13-120">Uma matriz de tabela hash que representa a Agenda diária</span><span class="sxs-lookup"><span data-stu-id="93f13-120">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f13-121">-DefaultProfile</span></span>
<span data-ttu-id="93f13-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93f13-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93f13-123">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="93f13-123">-Enabled</span></span>
<span data-ttu-id="93f13-124">A propriedade para decidir a política está habilitada ou não</span><span class="sxs-lookup"><span data-stu-id="93f13-124">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f13-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="93f13-125">-HourlySchedule</span></span>
<span data-ttu-id="93f13-126">Uma matriz de tabela hash que representa o Cronograma por hora</span><span class="sxs-lookup"><span data-stu-id="93f13-126">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f13-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93f13-127">-InputObject</span></span>
<span data-ttu-id="93f13-128">O objeto instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="93f13-128">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93f13-129">-Local</span><span class="sxs-lookup"><span data-stu-id="93f13-129">-Location</span></span>
<span data-ttu-id="93f13-130">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="93f13-130">The location of the resource</span></span>

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

### <span data-ttu-id="93f13-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="93f13-131">-MonthlySchedule</span></span>
<span data-ttu-id="93f13-132">Uma matriz de tabela hash que representa o cronograma montly</span><span class="sxs-lookup"><span data-stu-id="93f13-132">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f13-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="93f13-133">-Name</span></span>
<span data-ttu-id="93f13-134">O nome da política de instantâneo da ANF</span><span class="sxs-lookup"><span data-stu-id="93f13-134">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f13-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f13-135">-ResourceGroupName</span></span>
<span data-ttu-id="93f13-136">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="93f13-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="93f13-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93f13-137">-ResourceId</span></span>
<span data-ttu-id="93f13-138">A ID do recurso da Política de Instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="93f13-138">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="93f13-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="93f13-139">-Tag</span></span>
<span data-ttu-id="93f13-140">Uma matriz de tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="93f13-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="93f13-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="93f13-141">-WeeklySchedule</span></span>
<span data-ttu-id="93f13-142">Uma matriz de tabela hash que representa o cronograma montly</span><span class="sxs-lookup"><span data-stu-id="93f13-142">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f13-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="93f13-143">-Confirm</span></span>
<span data-ttu-id="93f13-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93f13-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93f13-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93f13-145">-WhatIf</span></span>
<span data-ttu-id="93f13-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="93f13-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93f13-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93f13-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93f13-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f13-148">CommonParameters</span></span>
<span data-ttu-id="93f13-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f13-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f13-150">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93f13-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f13-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="93f13-151">INPUTS</span></span>

### <span data-ttu-id="93f13-152">System.String</span><span class="sxs-lookup"><span data-stu-id="93f13-152">System.String</span></span>

### <span data-ttu-id="93f13-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="93f13-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="93f13-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="93f13-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="93f13-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="93f13-155">OUTPUTS</span></span>

### <span data-ttu-id="93f13-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="93f13-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="93f13-157">Notas</span><span class="sxs-lookup"><span data-stu-id="93f13-157">NOTES</span></span>

## <span data-ttu-id="93f13-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93f13-158">RELATED LINKS</span></span>
