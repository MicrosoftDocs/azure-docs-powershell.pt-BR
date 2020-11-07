---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945935"
---
# <span data-ttu-id="d5dc5-101">Test-AzureTrafficManagerDomainName</span><span class="sxs-lookup"><span data-stu-id="d5dc5-101">Test-AzureTrafficManagerDomainName</span></span>

## <span data-ttu-id="d5dc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="d5dc5-103">Verifica se um nome de domínio está disponível como um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="d5dc5-103">Checks whether a domain name is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="d5dc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5dc5-104">SYNTAX</span></span>

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d5dc5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5dc5-105">DESCRIPTION</span></span>
<span data-ttu-id="d5dc5-106">O cmdlet **Test-AzureTrafficManagerDomainName** verifica se um nome de domínio está disponível como um perfil do Gerenciador de tráfego do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5dc5-106">The **Test-AzureTrafficManagerDomainName** cmdlet checks whether a domain name is available as a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="d5dc5-107">Se o nome de domínio estiver disponível, esse cmdlet retornará um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="d5dc5-107">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="d5dc5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5dc5-108">EXAMPLES</span></span>

### <span data-ttu-id="d5dc5-109">Exemplo 1: verificar se um nome de domínio está disponível</span><span class="sxs-lookup"><span data-stu-id="d5dc5-109">Example 1: Check whether a domain name is available</span></span>
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

<span data-ttu-id="d5dc5-110">Esse comando verifica se o nome de domínio ContosoApp.trafficmanager.net está disponível como um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="d5dc5-110">This command checks whether the domain name ContosoApp.trafficmanager.net is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="d5dc5-111">OS</span><span class="sxs-lookup"><span data-stu-id="d5dc5-111">PARAMETERS</span></span>

### <span data-ttu-id="d5dc5-112">-DomainName</span><span class="sxs-lookup"><span data-stu-id="d5dc5-112">-DomainName</span></span>
<span data-ttu-id="d5dc5-113">Especifica o nome de domínio a ser testado.</span><span class="sxs-lookup"><span data-stu-id="d5dc5-113">Specifies the domain name to test.</span></span>
<span data-ttu-id="d5dc5-114">Você deve incluir a seguinte cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="d5dc5-114">You must include the following string:</span></span> 

<span data-ttu-id="d5dc5-115">. trafficmanager.net</span><span class="sxs-lookup"><span data-stu-id="d5dc5-115">.trafficmanager.net</span></span>

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

### <span data-ttu-id="d5dc5-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d5dc5-116">-Profile</span></span>
<span data-ttu-id="d5dc5-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d5dc5-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d5dc5-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d5dc5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5dc5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5dc5-119">CommonParameters</span></span>
<span data-ttu-id="d5dc5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5dc5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5dc5-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5dc5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5dc5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5dc5-122">INPUTS</span></span>

## <span data-ttu-id="d5dc5-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5dc5-123">OUTPUTS</span></span>

### <span data-ttu-id="d5dc5-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5dc5-124">System.Boolean</span></span>
<span data-ttu-id="d5dc5-125">Este cmdlet gera $True ou $False.</span><span class="sxs-lookup"><span data-stu-id="d5dc5-125">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="d5dc5-126">Se o nome de domínio estiver disponível, esse cmdlet retornará um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="d5dc5-126">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="d5dc5-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5dc5-127">NOTES</span></span>

## <span data-ttu-id="d5dc5-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5dc5-128">RELATED LINKS</span></span>

