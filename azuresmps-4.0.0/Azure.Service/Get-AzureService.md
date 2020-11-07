---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946309"
---
# <span data-ttu-id="9413b-101">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="9413b-101">Get-AzureService</span></span>

## <span data-ttu-id="9413b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9413b-102">SYNOPSIS</span></span>
<span data-ttu-id="9413b-103">Retorna um objeto com informações sobre os serviços de nuvem para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9413b-103">Returns an object with information about the cloud services for the current subscription.</span></span>

## <span data-ttu-id="9413b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9413b-104">SYNTAX</span></span>

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9413b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9413b-105">DESCRIPTION</span></span>
<span data-ttu-id="9413b-106">O cmdlet **Get-AzureService** retorna um objeto List com todos os serviços de nuvem do Azure associados à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9413b-106">The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.</span></span>
<span data-ttu-id="9413b-107">Se você especificar o parâmetro *ServiceName* , **Get-AzureService** retornará apenas as informações sobre o serviço correspondente.</span><span class="sxs-lookup"><span data-stu-id="9413b-107">If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.</span></span>

## <span data-ttu-id="9413b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9413b-108">EXAMPLES</span></span>

### <span data-ttu-id="9413b-109">Exemplo 1: obter informações sobre todos os serviços</span><span class="sxs-lookup"><span data-stu-id="9413b-109">Example 1: Get information about all services</span></span>
```
PS C:\> Get-AzureService
```

<span data-ttu-id="9413b-110">Esse comando retorna um objeto que contém informações sobre todos os serviços do Azure associados à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9413b-110">This command returns an object that contains information about all of the Azure services associated with the current subscription.</span></span>

### <span data-ttu-id="9413b-111">Exemplo 2: obter informações sobre um serviço especificado</span><span class="sxs-lookup"><span data-stu-id="9413b-111">Example 2: Get information about a specified service</span></span>
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

<span data-ttu-id="9413b-112">Esse comando retorna informações sobre o serviço de $MySvc.</span><span class="sxs-lookup"><span data-stu-id="9413b-112">This command returns information about the $MySvc service.</span></span>

### <span data-ttu-id="9413b-113">Exemplo 3: Exibir métodos e propriedades disponíveis</span><span class="sxs-lookup"><span data-stu-id="9413b-113">Example 3: Display available methods and properties</span></span>
```
PS C:\> Get-AzureService | Get-Member
```

<span data-ttu-id="9413b-114">Esse comando exibe as propriedades e os métodos que estão disponíveis a partir do cmdlet **Get-AzureService** .</span><span class="sxs-lookup"><span data-stu-id="9413b-114">This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.</span></span>

## <span data-ttu-id="9413b-115">OS</span><span class="sxs-lookup"><span data-stu-id="9413b-115">PARAMETERS</span></span>

### <span data-ttu-id="9413b-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9413b-116">-InformationAction</span></span>
<span data-ttu-id="9413b-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="9413b-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9413b-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9413b-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9413b-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="9413b-119">Continue</span></span>
- <span data-ttu-id="9413b-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9413b-120">Ignore</span></span>
- <span data-ttu-id="9413b-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="9413b-121">Inquire</span></span>
- <span data-ttu-id="9413b-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9413b-122">SilentlyContinue</span></span>
- <span data-ttu-id="9413b-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="9413b-123">Stop</span></span>
- <span data-ttu-id="9413b-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="9413b-124">Suspend</span></span>

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

### <span data-ttu-id="9413b-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9413b-125">-InformationVariable</span></span>
<span data-ttu-id="9413b-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="9413b-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9413b-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9413b-127">-Profile</span></span>
<span data-ttu-id="9413b-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9413b-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9413b-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9413b-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9413b-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9413b-130">-ServiceName</span></span>
<span data-ttu-id="9413b-131">Especifica o nome de um serviço no qual você deve retornar informações.</span><span class="sxs-lookup"><span data-stu-id="9413b-131">Specifies the name of a service on which to return information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9413b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9413b-132">CommonParameters</span></span>
<span data-ttu-id="9413b-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9413b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9413b-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9413b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9413b-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9413b-135">INPUTS</span></span>

## <span data-ttu-id="9413b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9413b-136">OUTPUTS</span></span>

### <span data-ttu-id="9413b-137">HostedServiceContext</span><span class="sxs-lookup"><span data-stu-id="9413b-137">HostedServiceContext</span></span>

## <span data-ttu-id="9413b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9413b-138">NOTES</span></span>

## <span data-ttu-id="9413b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9413b-139">RELATED LINKS</span></span>

[<span data-ttu-id="9413b-140">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="9413b-140">New-AzureService</span></span>](./New-AzureService.md)

[<span data-ttu-id="9413b-141">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="9413b-141">Set-AzureService</span></span>](./Set-AzureService.md)


