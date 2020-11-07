---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945434"
---
# <span data-ttu-id="80d45-101">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80d45-101">Set-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="80d45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80d45-102">SYNOPSIS</span></span>
<span data-ttu-id="80d45-103">Atualiza as propriedades de um ponto de extremidade em um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="80d45-103">Updates the properties of an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="80d45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80d45-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="80d45-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80d45-105">DESCRIPTION</span></span>
<span data-ttu-id="80d45-106">O cmdlet **set-AzureTrafficManagerEndpoint** atualiza as propriedades de um ponto de extremidade em um perfil do Gerenciador de tráfego do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="80d45-106">The **Set-AzureTrafficManagerEndpoint** cmdlet updates the properties of an endpoint in a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="80d45-107">Se o ponto de extremidade não existir no perfil atual, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="80d45-107">If the endpoint does not exist in the current profile, this cmdlet creates it.</span></span>
<span data-ttu-id="80d45-108">Depois de adicionar um ponto de extremidade, passe o resultado para o cmdlet **set-AzureTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="80d45-108">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="80d45-109">Esse cmdlet se conecta ao Azure para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="80d45-109">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="80d45-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80d45-110">EXAMPLES</span></span>

### <span data-ttu-id="80d45-111">Exemplo 1: atualizar um ponto de extremidade para um perfil</span><span class="sxs-lookup"><span data-stu-id="80d45-111">Example 1: Update an endpoint for a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="80d45-112">O primeiro comando usa o cmdlet **Get-AzureTrafficManagerProfile** para obter o perfil chamado ContosoProfile e, em seguida, armazena-o na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="80d45-112">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="80d45-113">O segundo comando atualiza o ponto de extremidade no perfil do Gerenciador de tráfego que está armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="80d45-113">The second command updates the endpoint in the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="80d45-114">O ponto de extremidade tem o nome de domínio ContosoApp02.cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="80d45-114">The endpoint has the domain name ContosoApp02.cloudapp.net.</span></span>
<span data-ttu-id="80d45-115">O comando também especifica o status, o tipo, a espessura e o local do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="80d45-115">The command also specifies the status, type, weight, and location of the endpoint.</span></span>
<span data-ttu-id="80d45-116">O comando passa o perfil modificado para o cmdlet **set-AzureTrafficManagerProfile** para se conectar ao Azure para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="80d45-116">The command passes the modified profile to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="80d45-117">OS</span><span class="sxs-lookup"><span data-stu-id="80d45-117">PARAMETERS</span></span>

### <span data-ttu-id="80d45-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="80d45-118">-DomainName</span></span>
<span data-ttu-id="80d45-119">Especifica o nome de domínio do ponto de extremidade a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="80d45-119">Specifies the domain name of the endpoint to modify.</span></span>

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

### <span data-ttu-id="80d45-120">-Local</span><span class="sxs-lookup"><span data-stu-id="80d45-120">-Location</span></span>
<span data-ttu-id="80d45-121">Especifica o local do ponto de extremidade que o cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="80d45-121">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="80d45-122">Deve ser um local do Azure.</span><span class="sxs-lookup"><span data-stu-id="80d45-122">This must be an Azure location.</span></span>

<span data-ttu-id="80d45-123">Esse parâmetro deve conter um valor de pontos de extremidade do tipo "any" ou do tipo "Trafficmanager" em um perfil que tenha o método de balanceamento de carga definido como "performance".</span><span class="sxs-lookup"><span data-stu-id="80d45-123">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="80d45-124">Os valores possíveis são os nomes de região do Azure, conforme listado em  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="80d45-124">The possible values are the Azure region names, as listed at  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="80d45-125">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="80d45-125">-MinChildEndpoints</span></span>
<span data-ttu-id="80d45-126">Especifica o número mínimo de pontos de extremidade que o perfil aninhado deve ter online para que este ponto de extremidade seja considerado online.</span><span class="sxs-lookup"><span data-stu-id="80d45-126">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="80d45-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="80d45-127">-Profile</span></span>
<span data-ttu-id="80d45-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="80d45-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="80d45-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="80d45-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80d45-130">-Status</span><span class="sxs-lookup"><span data-stu-id="80d45-130">-Status</span></span>
<span data-ttu-id="80d45-131">Especifica o status do ponto de extremidade de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="80d45-131">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="80d45-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="80d45-132">Valid values are:</span></span> 

- <span data-ttu-id="80d45-133">Possibilita</span><span class="sxs-lookup"><span data-stu-id="80d45-133">Enabled</span></span>
- <span data-ttu-id="80d45-134">Ativo</span><span class="sxs-lookup"><span data-stu-id="80d45-134">Disabled</span></span>

<span data-ttu-id="80d45-135">Se você especificar um valor habilitado, o Gerenciador de tráfego monitorará o ponto de extremidade e o método de balanceamento de carga o considerará ao gerenciar o tráfego.</span><span class="sxs-lookup"><span data-stu-id="80d45-135">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="80d45-136">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="80d45-136">-TrafficManagerProfile</span></span>
<span data-ttu-id="80d45-137">Especifica o objeto de perfil do Gerenciador de tráfego para o qual modificar o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="80d45-137">Specifies the Traffic Manager profile object for which to modify the endpoint.</span></span>

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

### <span data-ttu-id="80d45-138">-Digite</span><span class="sxs-lookup"><span data-stu-id="80d45-138">-Type</span></span>
<span data-ttu-id="80d45-139">Especifica o tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="80d45-139">Specifies the type of endpoint.</span></span>
<span data-ttu-id="80d45-140">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="80d45-140">Valid values are:</span></span> 

- <span data-ttu-id="80d45-141">CloudService</span><span class="sxs-lookup"><span data-stu-id="80d45-141">CloudService</span></span>
- <span data-ttu-id="80d45-142">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="80d45-142">AzureWebsite</span></span>
- <span data-ttu-id="80d45-143">Trafficmanager</span><span class="sxs-lookup"><span data-stu-id="80d45-143">TrafficManager</span></span>

- <span data-ttu-id="80d45-144">Qualquer</span><span class="sxs-lookup"><span data-stu-id="80d45-144">Any</span></span> 

<span data-ttu-id="80d45-145">Se houver mais de um ponto de extremidade AzureWebsite, os pontos de extremidade deverão estar em datacenters diferentes.</span><span class="sxs-lookup"><span data-stu-id="80d45-145">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="80d45-146">-Weight</span><span class="sxs-lookup"><span data-stu-id="80d45-146">-Weight</span></span>
<span data-ttu-id="80d45-147">Especifica a espessura do ponto de extremidade que o cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="80d45-147">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="80d45-148">O intervalo de valores válido para esse parâmetro é \[ 1, 1000 \] .</span><span class="sxs-lookup"><span data-stu-id="80d45-148">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="80d45-149">Esse parâmetro é usado apenas para políticas de balanceamento de carga do RoundRobin.</span><span class="sxs-lookup"><span data-stu-id="80d45-149">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="80d45-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d45-150">CommonParameters</span></span>
<span data-ttu-id="80d45-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d45-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d45-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80d45-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d45-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80d45-153">INPUTS</span></span>

## <span data-ttu-id="80d45-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80d45-154">OUTPUTS</span></span>

### <span data-ttu-id="80d45-155">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="80d45-155">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="80d45-156">Esse cmdlet gera um objeto de perfil do Gerenciador de tráfego, que contém informações sobre o perfil atualizado.</span><span class="sxs-lookup"><span data-stu-id="80d45-156">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="80d45-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80d45-157">NOTES</span></span>

## <span data-ttu-id="80d45-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80d45-158">RELATED LINKS</span></span>

[<span data-ttu-id="80d45-159">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80d45-159">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="80d45-160">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80d45-160">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="80d45-161">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="80d45-161">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="80d45-162">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="80d45-162">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


