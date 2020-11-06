---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: ee249d7379198a28cad22bf78a6c9ac1bf48f920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610775"
---
# <span data-ttu-id="e4e10-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e4e10-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="e4e10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4e10-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e10-103">Cria uma configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="e4e10-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4e10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4e10-104">SYNTAX</span></span>

### <span data-ttu-id="e4e10-105">Parâmetros para Add-AzureRmAutoscaleSetting cmdlet na semântica Update</span><span class="sxs-lookup"><span data-stu-id="e4e10-105">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4e10-106">Parâmetros para Add-AzureRmAutoscaleSetting cmdlet em Create Semantics</span><span class="sxs-lookup"><span data-stu-id="e4e10-106">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4e10-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4e10-107">DESCRIPTION</span></span>
<span data-ttu-id="e4e10-108">O cmdlet **Add-AzureRmAutoscaleSetting** cria uma configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="e4e10-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

## <span data-ttu-id="e4e10-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4e10-109">EXAMPLES</span></span>

### <span data-ttu-id="e4e10-110">Exemplo 1: criar uma configuração de autoescala</span><span class="sxs-lookup"><span data-stu-id="e4e10-110">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroup "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="e4e10-111">Os dois primeiros comandos usam New-AzureRmAutoscaleRule para criar duas regras de autoescala, $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="e4e10-111">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="e4e10-112">O terceiro e o quarto comandos usam New-AzureRmAutoscaleProfile para criar perfis de autoescala, $Profile 1 e $Profile 2, usando $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="e4e10-112">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="e4e10-113">O comando final cria uma configuração de autoescala usando os perfis em $Profile 1 e $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="e4e10-113">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="e4e10-114">OS</span><span class="sxs-lookup"><span data-stu-id="e4e10-114">PARAMETERS</span></span>

### <span data-ttu-id="e4e10-115">-AutoscaleProfiles</span><span class="sxs-lookup"><span data-stu-id="e4e10-115">-AutoscaleProfiles</span></span>
<span data-ttu-id="e4e10-116">Especifica uma lista de perfis a serem adicionados à configuração de autoescala ou $Null para adicionar sem perfil.</span><span class="sxs-lookup"><span data-stu-id="e4e10-116">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="e4e10-117">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="e4e10-117">-DisableSetting</span></span>
<span data-ttu-id="e4e10-118">Desabilita uma configuração de autoescala existente.</span><span class="sxs-lookup"><span data-stu-id="e4e10-118">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="e4e10-119">-Local</span><span class="sxs-lookup"><span data-stu-id="e4e10-119">-Location</span></span>
<span data-ttu-id="e4e10-120">Especifica o local da configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="e4e10-120">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e10-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4e10-121">-Name</span></span>
<span data-ttu-id="e4e10-122">Especifica o nome da configuração de dimensionamento automático a ser criada.</span><span class="sxs-lookup"><span data-stu-id="e4e10-122">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e10-123">-Notificações</span><span class="sxs-lookup"><span data-stu-id="e4e10-123">-Notifications</span></span>
<span data-ttu-id="e4e10-124">Especifica uma lista de notificações separadas por vírgula.</span><span class="sxs-lookup"><span data-stu-id="e4e10-124">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="e4e10-125">-Resource</span><span class="sxs-lookup"><span data-stu-id="e4e10-125">-ResourceGroup</span></span>
<span data-ttu-id="e4e10-126">Especifica o nome do grupo de recursos do recurso associado à configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="e4e10-126">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e10-127">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="e4e10-127">-SettingSpec</span></span>
<span data-ttu-id="e4e10-128">Especifica um objeto **AutoscaleSetting** .</span><span class="sxs-lookup"><span data-stu-id="e4e10-128">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="e4e10-129">Você pode usar o cmdlet Get-AzureRmAutoscaleSetting para obter um objeto **AutoscaleSetting** ou pode construir um em um script do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e4e10-129">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e10-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e4e10-130">-TargetResourceId</span></span>
<span data-ttu-id="e4e10-131">Especifica a ID do recurso para autoescala.</span><span class="sxs-lookup"><span data-stu-id="e4e10-131">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e10-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e10-132">-DefaultProfile</span></span>
<span data-ttu-id="e4e10-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e10-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e10-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e10-134">CommonParameters</span></span>
<span data-ttu-id="e4e10-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e10-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e10-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e10-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e10-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4e10-137">INPUTS</span></span>

## <span data-ttu-id="e4e10-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4e10-138">OUTPUTS</span></span>

### <span data-ttu-id="e4e10-139">Microsoft. Azure. Commands. insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e4e10-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="e4e10-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4e10-140">NOTES</span></span>

## <span data-ttu-id="e4e10-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4e10-141">RELATED LINKS</span></span>

[<span data-ttu-id="e4e10-142">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e4e10-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="e4e10-143">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="e4e10-143">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="e4e10-144">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="e4e10-144">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="e4e10-145">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e4e10-145">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


