---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946376"
---
# <span data-ttu-id="0b78c-101">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b78c-101">Add-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="0b78c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b78c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b78c-103">Adiciona um ponto de extremidade a um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="0b78c-103">Adds an endpoint to a Traffic Manager profile.</span></span>

## <span data-ttu-id="0b78c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b78c-104">SYNTAX</span></span>

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0b78c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b78c-105">DESCRIPTION</span></span>
<span data-ttu-id="0b78c-106">O cmdlet **Add-AzureTrafficManagerEndpoint** adiciona um ponto de extremidade a um perfil do Gerenciador de tráfego do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0b78c-106">The **Add-AzureTrafficManagerEndpoint** cmdlet adds an endpoint to a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="0b78c-107">Depois de adicionar um ponto de extremidade, passe o resultado para o cmdlet **set-AzureTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b78c-107">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0b78c-108">Esse cmdlet se conecta ao Azure para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="0b78c-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="0b78c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b78c-109">EXAMPLES</span></span>

### <span data-ttu-id="0b78c-110">Exemplo 1: adicionar um ponto de extremidade a um perfil</span><span class="sxs-lookup"><span data-stu-id="0b78c-110">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="0b78c-111">O primeiro comando usa o cmdlet **Get-AzureTrafficManagerProfile** para obter o perfil chamado ContosoProfile e, em seguida, armazena-o na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0b78c-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="0b78c-112">O segundo comando adiciona um ponto de extremidade ao perfil do Gerenciador de tráfego que está armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0b78c-112">The second command adds an endpoint to Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="0b78c-113">O ponto de extremidade tem o nome de domínio Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="0b78c-113">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="0b78c-114">O comando também especifica se ele está habilitado e seu tipo.</span><span class="sxs-lookup"><span data-stu-id="0b78c-114">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="0b78c-115">O comando passa o objeto de perfil para o cmdlet **set-AzureTrafficManagerProfile** para se conectar ao Azure para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="0b78c-115">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

### <span data-ttu-id="0b78c-116">Exemplo 2: adicionar um ponto de extremidade com local e peso especificado</span><span class="sxs-lookup"><span data-stu-id="0b78c-116">Example 2: Add an endpoint that has a specified location and weight</span></span>
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="0b78c-117">Esse comando adiciona um ponto de extremidade a um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="0b78c-117">This command adds an endpoint to a Traffic Manager profile.</span></span>
<span data-ttu-id="0b78c-118">O ponto de extremidade tem o nome de domínio Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="0b78c-118">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="0b78c-119">O comando também especifica se ele está habilitado e seu tipo.</span><span class="sxs-lookup"><span data-stu-id="0b78c-119">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="0b78c-120">O comando também especifica a espessura e o local da empresa.</span><span class="sxs-lookup"><span data-stu-id="0b78c-120">The command also specifies the weight and location for the endpoint.</span></span>
<span data-ttu-id="0b78c-121">O comando passa o objeto de perfil para **set-AzureTrafficManagerProfile** para se conectar ao Azure para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="0b78c-121">The command passes the profile object to **Set-AzureTrafficManagerProfile** to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="0b78c-122">OS</span><span class="sxs-lookup"><span data-stu-id="0b78c-122">PARAMETERS</span></span>

### <span data-ttu-id="0b78c-123">-DomainName</span><span class="sxs-lookup"><span data-stu-id="0b78c-123">-DomainName</span></span>
<span data-ttu-id="0b78c-124">Especifica o nome de domínio do ponto de extremidade a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0b78c-124">Specifies the domain name of the endpoint to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b78c-125">-Local</span><span class="sxs-lookup"><span data-stu-id="0b78c-125">-Location</span></span>
<span data-ttu-id="0b78c-126">Especifica o local do ponto de extremidade que o cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="0b78c-126">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="0b78c-127">Deve ser um local do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b78c-127">This must be an Azure location.</span></span>

<span data-ttu-id="0b78c-128">Esse parâmetro deve conter um valor de pontos de extremidade do tipo "any" ou do tipo "Trafficmanager" em um perfil que tenha o método de balanceamento de carga definido como "performance".</span><span class="sxs-lookup"><span data-stu-id="0b78c-128">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="0b78c-129">Os valores possíveis são os nomes de região do Azure, conforme listado em https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="0b78c-129">The possible values are the Azure region names, as listed at https://azure.microsoft.com/regions/.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b78c-130">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="0b78c-130">-MinChildEndpoints</span></span>
<span data-ttu-id="0b78c-131">Especifica o número mínimo de pontos de extremidade que o perfil aninhado deve ter online para que este ponto de extremidade seja considerado online.</span><span class="sxs-lookup"><span data-stu-id="0b78c-131">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b78c-132">-Perfil</span><span class="sxs-lookup"><span data-stu-id="0b78c-132">-Profile</span></span>
<span data-ttu-id="0b78c-133">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="0b78c-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0b78c-134">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="0b78c-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b78c-135">-Status</span><span class="sxs-lookup"><span data-stu-id="0b78c-135">-Status</span></span>
<span data-ttu-id="0b78c-136">Especifica o status do ponto de extremidade de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="0b78c-136">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="0b78c-137">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0b78c-137">Valid values are:</span></span> 

- <span data-ttu-id="0b78c-138">Possibilita</span><span class="sxs-lookup"><span data-stu-id="0b78c-138">Enabled</span></span>
- <span data-ttu-id="0b78c-139">Ativo</span><span class="sxs-lookup"><span data-stu-id="0b78c-139">Disabled</span></span>

<span data-ttu-id="0b78c-140">Se você especificar um valor habilitado, o Gerenciador de tráfego monitorará o ponto de extremidade e o método de balanceamento de carga o considerará ao gerenciar o tráfego.</span><span class="sxs-lookup"><span data-stu-id="0b78c-140">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b78c-141">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0b78c-141">-TrafficManagerProfile</span></span>
<span data-ttu-id="0b78c-142">Especifica o objeto de perfil do Gerenciador de tráfego ao qual adicionar o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="0b78c-142">Specifies the Traffic Manager profile object to which to add the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b78c-143">-Digite</span><span class="sxs-lookup"><span data-stu-id="0b78c-143">-Type</span></span>
<span data-ttu-id="0b78c-144">Especifica o tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="0b78c-144">Specifies the type of endpoint.</span></span>
<span data-ttu-id="0b78c-145">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0b78c-145">Valid values are:</span></span> 

- <span data-ttu-id="0b78c-146">CloudService</span><span class="sxs-lookup"><span data-stu-id="0b78c-146">CloudService</span></span>
- <span data-ttu-id="0b78c-147">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0b78c-147">AzureWebsite</span></span>
- <span data-ttu-id="0b78c-148">Trafficmanager</span><span class="sxs-lookup"><span data-stu-id="0b78c-148">TrafficManager</span></span>

- <span data-ttu-id="0b78c-149">Qualquer</span><span class="sxs-lookup"><span data-stu-id="0b78c-149">Any</span></span> 

<span data-ttu-id="0b78c-150">Se houver mais de um ponto de extremidade AzureWebsite, os pontos de extremidade deverão estar em datacenters diferentes.</span><span class="sxs-lookup"><span data-stu-id="0b78c-150">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b78c-151">-Weight</span><span class="sxs-lookup"><span data-stu-id="0b78c-151">-Weight</span></span>
<span data-ttu-id="0b78c-152">Especifica a espessura do ponto de extremidade que o cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="0b78c-152">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="0b78c-153">O intervalo de valores válido para esse parâmetro é \[ 1, 1000 \] .</span><span class="sxs-lookup"><span data-stu-id="0b78c-153">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="0b78c-154">Esse parâmetro é usado apenas para políticas de balanceamento de carga do RoundRobin.</span><span class="sxs-lookup"><span data-stu-id="0b78c-154">This parameter is only used for RoundRobin load balancing policies.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b78c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b78c-155">CommonParameters</span></span>
<span data-ttu-id="0b78c-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b78c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b78c-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b78c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b78c-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b78c-158">INPUTS</span></span>

## <span data-ttu-id="0b78c-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b78c-159">OUTPUTS</span></span>

### <span data-ttu-id="0b78c-160">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="0b78c-160">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="0b78c-161">Esse cmdlet gera um objeto de perfil do Gerenciador de tráfego, que contém informações sobre o perfil atualizado.</span><span class="sxs-lookup"><span data-stu-id="0b78c-161">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="0b78c-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b78c-162">NOTES</span></span>

## <span data-ttu-id="0b78c-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b78c-163">RELATED LINKS</span></span>

[<span data-ttu-id="0b78c-164">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b78c-164">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="0b78c-165">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b78c-165">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="0b78c-166">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0b78c-166">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="0b78c-167">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0b78c-167">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


