---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946244"
---
# <span data-ttu-id="54787-101">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="54787-101">Move-AzureDeployment</span></span>

## <span data-ttu-id="54787-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54787-102">SYNOPSIS</span></span>
<span data-ttu-id="54787-103">Troca implantações entre produção e preparação.</span><span class="sxs-lookup"><span data-stu-id="54787-103">Swaps deployments between production and staging.</span></span>

## <span data-ttu-id="54787-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54787-104">SYNTAX</span></span>

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="54787-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54787-105">DESCRIPTION</span></span>
<span data-ttu-id="54787-106">O cmdlet **move-AzureDeployment** troca os endereços IP virtuais de implantações em ambientes de produção e transferência.</span><span class="sxs-lookup"><span data-stu-id="54787-106">The **Move-AzureDeployment** cmdlet swaps the virtual IP addresses of deployments in production and staging environments.</span></span>
<span data-ttu-id="54787-107">Esse cmdlet troca uma implantação que atualmente é executada no ambiente de preparo para o ambiente de produção e uma implantação que é executada no ambiente de produção para o ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="54787-107">This cmdlet swaps a deployment that currently runs in the staging environment to the production environment, and a deployment that runs in the production environment to the staging environment.</span></span>
<span data-ttu-id="54787-108">Se houver uma implantação no ambiente de preparo e nenhuma implantação no ambiente de produção, o cmdlet moverá a implantação para produção.</span><span class="sxs-lookup"><span data-stu-id="54787-108">If there is a deployment in the staging environment and no deployment in the production environment, the cmdlet moves the deployment to production.</span></span>
<span data-ttu-id="54787-109">Se houver uma implantação no ambiente de produção e nenhuma implantação no ambiente de preparo, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="54787-109">If there is a deployment in the production environment and no deployment in the staging environment, the cmdlet fails.</span></span>

## <span data-ttu-id="54787-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54787-110">EXAMPLES</span></span>

### <span data-ttu-id="54787-111">Exemplo 1: trocar implantações de um serviço</span><span class="sxs-lookup"><span data-stu-id="54787-111">Example 1: Swap deployments for a service</span></span>
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="54787-112">Esse comando troca as implantações do serviço chamado ContosoService entre os ambientes de produção e transferência.</span><span class="sxs-lookup"><span data-stu-id="54787-112">This command swaps the deployments of the service named ContosoService between the production and staging environments.</span></span>

## <span data-ttu-id="54787-113">OS</span><span class="sxs-lookup"><span data-stu-id="54787-113">PARAMETERS</span></span>

### <span data-ttu-id="54787-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="54787-114">-InformationAction</span></span>
<span data-ttu-id="54787-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="54787-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="54787-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="54787-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54787-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="54787-117">Continue</span></span>
- <span data-ttu-id="54787-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="54787-118">Ignore</span></span>
- <span data-ttu-id="54787-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="54787-119">Inquire</span></span>
- <span data-ttu-id="54787-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="54787-120">SilentlyContinue</span></span>
- <span data-ttu-id="54787-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="54787-121">Stop</span></span>
- <span data-ttu-id="54787-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="54787-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54787-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="54787-123">-InformationVariable</span></span>
<span data-ttu-id="54787-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="54787-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54787-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="54787-125">-Profile</span></span>
<span data-ttu-id="54787-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="54787-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54787-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="54787-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54787-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="54787-128">-ServiceName</span></span>
<span data-ttu-id="54787-129">Especifica o nome do serviço para o qual esse cmdlet troca a produção e a transferência de implantações.</span><span class="sxs-lookup"><span data-stu-id="54787-129">Specifies the name of the service for which this cmdlet swaps production and staging deployments.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54787-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54787-130">CommonParameters</span></span>
<span data-ttu-id="54787-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54787-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54787-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54787-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54787-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54787-133">INPUTS</span></span>

## <span data-ttu-id="54787-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54787-134">OUTPUTS</span></span>

### <span data-ttu-id="54787-135">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="54787-135">ManagementOperationContext</span></span>

## <span data-ttu-id="54787-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54787-136">NOTES</span></span>

## <span data-ttu-id="54787-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54787-137">RELATED LINKS</span></span>

[<span data-ttu-id="54787-138">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="54787-138">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="54787-139">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="54787-139">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="54787-140">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="54787-140">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="54787-141">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="54787-141">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="54787-142">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="54787-142">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


