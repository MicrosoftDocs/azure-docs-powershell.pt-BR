---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945536"
---
# <span data-ttu-id="3373a-101">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3373a-101">Get-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="3373a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3373a-102">SYNOPSIS</span></span>
<span data-ttu-id="3373a-103">Obtém os detalhes de um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="3373a-103">Gets the details of a Traffic Manager profile.</span></span>

## <span data-ttu-id="3373a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3373a-104">SYNTAX</span></span>

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3373a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3373a-105">DESCRIPTION</span></span>
<span data-ttu-id="3373a-106">O cmdlet **Get-AzureTrafficManagerProfile** Obtém os detalhes de um perfil do Gerenciador de tráfego do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3373a-106">The **Get-AzureTrafficManagerProfile** cmdlet gets the details of a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="3373a-107">Se você não especificar o parâmetro *Name* , o cmdlet listará os perfis do Gerenciador de tráfego na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3373a-107">If you do not specify the *Name* parameter, the cmdlet lists the Traffic Manager profiles in the current subscription.</span></span>

## <span data-ttu-id="3373a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3373a-108">EXAMPLES</span></span>

### <span data-ttu-id="3373a-109">Exemplo 1: obter a lista de perfis do Gerenciador de tráfego em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="3373a-109">Example 1: Get the list of Traffic Manager profiles in a subscription</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile
```

<span data-ttu-id="3373a-110">Este comando obtém a lista de perfis do Gerenciador de tráfego na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="3373a-110">This command gets the list of Traffic Manager profiles in your subscription.</span></span>

### <span data-ttu-id="3373a-111">Exemplo 2: obter um perfil do Gerenciador de tráfego</span><span class="sxs-lookup"><span data-stu-id="3373a-111">Example 2: Get a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="3373a-112">Esse comando obtém o perfil do Gerenciador de tráfego chamado MyProfile.</span><span class="sxs-lookup"><span data-stu-id="3373a-112">This command gets the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="3373a-113">Exemplo 3: adicionar um ponto de extremidade a um perfil do Gerenciador de tráfego</span><span class="sxs-lookup"><span data-stu-id="3373a-113">Example 3: Add an endpoint to a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="3373a-114">Esse comando adiciona um ponto de extremidade a um perfil do Gerenciador de tráfego e, em seguida, salva o perfil.</span><span class="sxs-lookup"><span data-stu-id="3373a-114">This command adds an endpoint to a Traffic Manager profile, and then saves the profile.</span></span>

## <span data-ttu-id="3373a-115">OS</span><span class="sxs-lookup"><span data-stu-id="3373a-115">PARAMETERS</span></span>

### <span data-ttu-id="3373a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3373a-116">-Name</span></span>
<span data-ttu-id="3373a-117">Especifica o nome do perfil do Gerenciador de tráfego a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="3373a-117">Specifies the name of the Traffic Manager profile to get.</span></span>

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

### <span data-ttu-id="3373a-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3373a-118">-Profile</span></span>
<span data-ttu-id="3373a-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3373a-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3373a-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3373a-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3373a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3373a-121">CommonParameters</span></span>
<span data-ttu-id="3373a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3373a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3373a-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3373a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3373a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3373a-124">INPUTS</span></span>

## <span data-ttu-id="3373a-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3373a-125">OUTPUTS</span></span>

### <span data-ttu-id="3373a-126">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="3373a-126">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="3373a-127">Esse cmdlet gera um objeto ou objetos de perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="3373a-127">This cmdlet generates a Traffic Manager profile object or objects.</span></span>

## <span data-ttu-id="3373a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3373a-128">NOTES</span></span>

## <span data-ttu-id="3373a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3373a-129">RELATED LINKS</span></span>

[<span data-ttu-id="3373a-130">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3373a-130">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="3373a-131">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3373a-131">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3373a-132">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3373a-132">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3373a-133">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3373a-133">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3373a-134">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3373a-134">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3373a-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3373a-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


