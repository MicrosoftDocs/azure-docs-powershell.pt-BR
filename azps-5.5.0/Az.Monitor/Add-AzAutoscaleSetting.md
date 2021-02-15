---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: b2f7410f45a5b60a768d22fe7e66b7d8c1e4ad94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112966"
---
# <span data-ttu-id="f27c8-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f27c8-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="f27c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f27c8-102">SYNOPSIS</span></span>
<span data-ttu-id="f27c8-103">Cria uma configuração de Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="f27c8-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="f27c8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f27c8-104">SYNTAX</span></span>

### <span data-ttu-id="f27c8-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f27c8-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f27c8-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f27c8-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f27c8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f27c8-107">DESCRIPTION</span></span>
<span data-ttu-id="f27c8-108">O **cmdlet Add-AzAutoscaleSetting** cria uma configuração de Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="f27c8-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="f27c8-109">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="f27c8-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f27c8-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f27c8-110">EXAMPLES</span></span>

### <span data-ttu-id="f27c8-111">Exemplo 1: Criar uma configuração de Escala Automática</span><span class="sxs-lookup"><span data-stu-id="f27c8-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="f27c8-112">Os dois primeiros comandos usam [o New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) para criar duas regras de Escala automática, $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="f27c8-112">The first two commands use [New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="f27c8-113">O terceiro e o quarto comandos usam o [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) para criar perfis de Escala Automática, $Profile 1 e $Profile 2, usando $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="f27c8-113">The third and fourth commands use [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="f27c8-114">O comando final cria uma configuração de Escala Automática usando os perfis $Profile 1 e $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="f27c8-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="f27c8-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f27c8-115">PARAMETERS</span></span>

### <span data-ttu-id="f27c8-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="f27c8-116">-AutoscaleProfile</span></span>
<span data-ttu-id="f27c8-117">Especifica uma lista de perfis para adicionar à configuração de Escala Automática ou $Null adicionar nenhum perfil.</span><span class="sxs-lookup"><span data-stu-id="f27c8-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f27c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27c8-118">-DefaultProfile</span></span>
<span data-ttu-id="f27c8-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f27c8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f27c8-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="f27c8-120">-DisableSetting</span></span>
<span data-ttu-id="f27c8-121">Desabilita uma configuração de Escala automática existente.</span><span class="sxs-lookup"><span data-stu-id="f27c8-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f27c8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f27c8-122">-InputObject</span></span>
<span data-ttu-id="f27c8-123">A especificação completa de uma AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f27c8-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f27c8-124">-Local</span><span class="sxs-lookup"><span data-stu-id="f27c8-124">-Location</span></span>
<span data-ttu-id="f27c8-125">Especifica o local da configuração de Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="f27c8-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f27c8-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f27c8-126">-Name</span></span>
<span data-ttu-id="f27c8-127">Especifica o nome da configuração de Escala Automática a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f27c8-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f27c8-128">-Notificação</span><span class="sxs-lookup"><span data-stu-id="f27c8-128">-Notification</span></span>
<span data-ttu-id="f27c8-129">Especifica uma lista de notificações separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="f27c8-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f27c8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f27c8-130">-ResourceGroupName</span></span>
<span data-ttu-id="f27c8-131">Especifica o nome do grupo de recursos do recurso associado à configuração de Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="f27c8-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f27c8-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f27c8-132">-TargetResourceId</span></span>
<span data-ttu-id="f27c8-133">Especifica a ID do recurso para escala automática.</span><span class="sxs-lookup"><span data-stu-id="f27c8-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f27c8-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f27c8-134">-Confirm</span></span>
<span data-ttu-id="f27c8-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f27c8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f27c8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f27c8-136">-WhatIf</span></span>
<span data-ttu-id="f27c8-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f27c8-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f27c8-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f27c8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f27c8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27c8-139">CommonParameters</span></span>
<span data-ttu-id="f27c8-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f27c8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27c8-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f27c8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27c8-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="f27c8-142">INPUTS</span></span>

### <span data-ttu-id="f27c8-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f27c8-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="f27c8-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f27c8-144">System.String</span></span>

### <span data-ttu-id="f27c8-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f27c8-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f27c8-146">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f27c8-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f27c8-147">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f27c8-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f27c8-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="f27c8-148">OUTPUTS</span></span>

### <span data-ttu-id="f27c8-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f27c8-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="f27c8-150">Notas</span><span class="sxs-lookup"><span data-stu-id="f27c8-150">NOTES</span></span>

## <span data-ttu-id="f27c8-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f27c8-151">RELATED LINKS</span></span>

[<span data-ttu-id="f27c8-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f27c8-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="f27c8-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="f27c8-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="f27c8-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="f27c8-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="f27c8-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f27c8-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


