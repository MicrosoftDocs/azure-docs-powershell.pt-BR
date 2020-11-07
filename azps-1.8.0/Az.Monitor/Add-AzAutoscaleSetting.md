---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: c25d86f9496222311aab6c92f9ce40edb1e5e911
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770352"
---
# <span data-ttu-id="1f4e2-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1f4e2-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="1f4e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4e2-103">Cria uma configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="1f4e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f4e2-104">SYNTAX</span></span>

### <span data-ttu-id="1f4e2-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1f4e2-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f4e2-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1f4e2-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f4e2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f4e2-107">DESCRIPTION</span></span>
<span data-ttu-id="1f4e2-108">O cmdlet **Add-AzAutoscaleSetting** cria uma configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="1f4e2-109">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="1f4e2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f4e2-110">EXAMPLES</span></span>

### <span data-ttu-id="1f4e2-111">Exemplo 1: criar uma configuração de autoescala</span><span class="sxs-lookup"><span data-stu-id="1f4e2-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="1f4e2-112">Os dois primeiros comandos usam New-AzAutoscaleRule para criar duas regras de autoescala, $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-112">The first two commands use New-AzAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="1f4e2-113">O terceiro e o quarto comandos usam New-AzAutoscaleProfile para criar perfis de autoescala, $Profile 1 e $Profile 2, usando $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-113">The third and fourth commands use New-AzAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="1f4e2-114">O comando final cria uma configuração de autoescala usando os perfis em $Profile 1 e $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="1f4e2-115">OS</span><span class="sxs-lookup"><span data-stu-id="1f4e2-115">PARAMETERS</span></span>

### <span data-ttu-id="1f4e2-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="1f4e2-116">-AutoscaleProfile</span></span>
<span data-ttu-id="1f4e2-117">Especifica uma lista de perfis a serem adicionados à configuração de autoescala ou $Null para adicionar sem perfil.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="1f4e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4e2-118">-DefaultProfile</span></span>
<span data-ttu-id="1f4e2-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1f4e2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f4e2-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="1f4e2-120">-DisableSetting</span></span>
<span data-ttu-id="1f4e2-121">Desabilita uma configuração de autoescala existente.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="1f4e2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f4e2-122">-InputObject</span></span>
<span data-ttu-id="1f4e2-123">A especificação completa de um AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1f4e2-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="1f4e2-124">-Local</span><span class="sxs-lookup"><span data-stu-id="1f4e2-124">-Location</span></span>
<span data-ttu-id="1f4e2-125">Especifica o local da configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="1f4e2-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f4e2-126">-Name</span></span>
<span data-ttu-id="1f4e2-127">Especifica o nome da configuração de dimensionamento automático a ser criada.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="1f4e2-128">-Notificação</span><span class="sxs-lookup"><span data-stu-id="1f4e2-128">-Notification</span></span>
<span data-ttu-id="1f4e2-129">Especifica uma lista de notificações separadas por vírgula.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="1f4e2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4e2-130">-ResourceGroupName</span></span>
<span data-ttu-id="1f4e2-131">Especifica o nome do grupo de recursos do recurso associado à configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="1f4e2-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1f4e2-132">-TargetResourceId</span></span>
<span data-ttu-id="1f4e2-133">Especifica a ID do recurso para autoescala.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="1f4e2-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f4e2-134">-Confirm</span></span>
<span data-ttu-id="1f4e2-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f4e2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f4e2-136">-WhatIf</span></span>
<span data-ttu-id="1f4e2-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f4e2-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f4e2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4e2-139">CommonParameters</span></span>
<span data-ttu-id="1f4e2-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f4e2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4e2-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f4e2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4e2-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f4e2-142">INPUTS</span></span>

### <span data-ttu-id="1f4e2-143">Microsoft. Azure. Commands. insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1f4e2-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="1f4e2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1f4e2-144">System.String</span></span>

### <span data-ttu-id="1f4e2-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1f4e2-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1f4e2-146">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. monitor. Management. Models. AutoscaleProfile, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1f4e2-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1f4e2-147">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1f4e2-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1f4e2-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f4e2-148">OUTPUTS</span></span>

### <span data-ttu-id="1f4e2-149">Microsoft. Azure. Commands. insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1f4e2-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="1f4e2-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f4e2-150">NOTES</span></span>

## <span data-ttu-id="1f4e2-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f4e2-151">RELATED LINKS</span></span>

[<span data-ttu-id="1f4e2-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1f4e2-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="1f4e2-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="1f4e2-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="1f4e2-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="1f4e2-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="1f4e2-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1f4e2-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


