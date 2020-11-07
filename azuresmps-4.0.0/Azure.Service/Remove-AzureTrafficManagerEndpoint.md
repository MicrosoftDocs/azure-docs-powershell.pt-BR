---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946092"
---
# <span data-ttu-id="d16a1-101">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d16a1-101">Remove-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="d16a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d16a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d16a1-103">Remove um ponto de extremidade de um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="d16a1-103">Removes an endpoint from a Traffic Manager profile.</span></span>

## <span data-ttu-id="d16a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d16a1-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d16a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d16a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d16a1-106">O cmdlet **Remove-AzureTrafficManagerEndpoint** remove um ponto de extremidade de um perfil do Gerenciador de tráfego do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d16a1-106">The **Remove-AzureTrafficManagerEndpoint** cmdlet removes an endpoint from a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="d16a1-107">Depois de remover um ponto de extremidade, passe o resultado para o cmdlet **set-AzureTrafficManagerProfile** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="d16a1-107">After you remove an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d16a1-108">Esse cmdlet se conecta ao Azure para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="d16a1-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="d16a1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d16a1-109">EXAMPLES</span></span>

### <span data-ttu-id="d16a1-110">Exemplo 1: remover um ponto de extremidade de um perfil</span><span class="sxs-lookup"><span data-stu-id="d16a1-110">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="d16a1-111">O primeiro comando usa o cmdlet **Get-AzureTrafficManagerProfile** para obter o perfil chamado ContosoProfile e, em seguida, armazena-o na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d16a1-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="d16a1-112">O segundo comando Remove um ponto de extremidade que tem o nome de domínio Contoso02App.cloudapp.net do perfil do Gerenciador de tráfego que está armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d16a1-112">The second command removes an endpoint that has the domain name Contoso02App.cloudapp.net from the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="d16a1-113">O comando passa o objeto de perfil para o cmdlet **set-AzureTrafficManagerProfile** para se conectar ao Azure para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="d16a1-113">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="d16a1-114">OS</span><span class="sxs-lookup"><span data-stu-id="d16a1-114">PARAMETERS</span></span>

### <span data-ttu-id="d16a1-115">-DomainName</span><span class="sxs-lookup"><span data-stu-id="d16a1-115">-DomainName</span></span>
<span data-ttu-id="d16a1-116">Especifica o nome de domínio do ponto de extremidade a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d16a1-116">Specifies the domain name of the endpoint to remove.</span></span>

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

### <span data-ttu-id="d16a1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d16a1-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16a1-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d16a1-118">-Profile</span></span>
<span data-ttu-id="d16a1-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d16a1-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d16a1-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d16a1-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d16a1-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d16a1-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="d16a1-122">Especifica o objeto de perfil do Gerenciador de tráfego do qual o ponto de extremidade será removido.</span><span class="sxs-lookup"><span data-stu-id="d16a1-122">Specifies the Traffic Manager profile object from which to remove the endpoint.</span></span>

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

### <span data-ttu-id="d16a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16a1-123">CommonParameters</span></span>
<span data-ttu-id="d16a1-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d16a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d16a1-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d16a1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16a1-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d16a1-126">INPUTS</span></span>

## <span data-ttu-id="d16a1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d16a1-127">OUTPUTS</span></span>

### <span data-ttu-id="d16a1-128">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="d16a1-128">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="d16a1-129">Esse cmdlet gera um objeto de perfil do Gerenciador de tráfego, que contém informações sobre o perfil atualizado.</span><span class="sxs-lookup"><span data-stu-id="d16a1-129">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="d16a1-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d16a1-130">NOTES</span></span>

## <span data-ttu-id="d16a1-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d16a1-131">RELATED LINKS</span></span>

[<span data-ttu-id="d16a1-132">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d16a1-132">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="d16a1-133">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d16a1-133">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="d16a1-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d16a1-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d16a1-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d16a1-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


