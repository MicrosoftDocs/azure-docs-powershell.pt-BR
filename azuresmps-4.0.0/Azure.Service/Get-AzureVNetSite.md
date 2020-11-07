---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946527"
---
# <span data-ttu-id="bf78c-101">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="bf78c-101">Get-AzureVNetSite</span></span>

## <span data-ttu-id="bf78c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf78c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf78c-103">Obtém um objeto List com informações sobre as redes virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf78c-103">Gets a list object with information about Azure virtual networks.</span></span>

## <span data-ttu-id="bf78c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf78c-104">SYNTAX</span></span>

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bf78c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf78c-105">DESCRIPTION</span></span>
<span data-ttu-id="bf78c-106">O cmdlet **Get-AzureVNetSite** Obtém um objeto List com informações sobre as redes virtuais do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="bf78c-106">The **Get-AzureVNetSite** cmdlet gets a list object with information about Azure virtual networks for the current subscription.</span></span>
<span data-ttu-id="bf78c-107">Se você especificar um nome de rede virtual, somente as informações dessa rede virtual serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="bf78c-107">If you specify a virtual network name, only information for that virtual network is returned.</span></span>

## <span data-ttu-id="bf78c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf78c-108">EXAMPLES</span></span>

### <span data-ttu-id="bf78c-109">Exemplo 1: obter informações sobre todas as redes virtuais na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="bf78c-109">Example 1: Get information about all virtual networks in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite
```

<span data-ttu-id="bf78c-110">Esse comando obtém informações sobre todas as redes virtuais na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="bf78c-110">This command gets information about all the virtual networks in the current subscription.</span></span>

### <span data-ttu-id="bf78c-111">Exemplo 2: obter informações sobre uma rede virtual específica na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="bf78c-111">Example 2: Get information about a specific virtual network in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

<span data-ttu-id="bf78c-112">Esse comando recupera informações somente na rede virtual MyProductionNetwork.</span><span class="sxs-lookup"><span data-stu-id="bf78c-112">This command retrieves information on the MyProductionNetwork virtual network only.</span></span>

## <span data-ttu-id="bf78c-113">OS</span><span class="sxs-lookup"><span data-stu-id="bf78c-113">PARAMETERS</span></span>

### <span data-ttu-id="bf78c-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bf78c-114">-InformationAction</span></span>
<span data-ttu-id="bf78c-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="bf78c-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bf78c-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bf78c-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf78c-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="bf78c-117">Continue</span></span>
- <span data-ttu-id="bf78c-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="bf78c-118">Ignore</span></span>
- <span data-ttu-id="bf78c-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="bf78c-119">Inquire</span></span>
- <span data-ttu-id="bf78c-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bf78c-120">SilentlyContinue</span></span>
- <span data-ttu-id="bf78c-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="bf78c-121">Stop</span></span>
- <span data-ttu-id="bf78c-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="bf78c-122">Suspend</span></span>

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

### <span data-ttu-id="bf78c-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bf78c-123">-InformationVariable</span></span>
<span data-ttu-id="bf78c-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="bf78c-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bf78c-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bf78c-125">-Profile</span></span>
<span data-ttu-id="bf78c-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bf78c-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf78c-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bf78c-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf78c-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="bf78c-128">-VNetName</span></span>
<span data-ttu-id="bf78c-129">Especifica um nome de rede virtual para o qual as informações são retornadas.</span><span class="sxs-lookup"><span data-stu-id="bf78c-129">Specifies a virtual network name to return information about.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf78c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf78c-130">CommonParameters</span></span>
<span data-ttu-id="bf78c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf78c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf78c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf78c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf78c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf78c-133">INPUTS</span></span>

## <span data-ttu-id="bf78c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf78c-134">OUTPUTS</span></span>

## <span data-ttu-id="bf78c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf78c-135">NOTES</span></span>

## <span data-ttu-id="bf78c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf78c-136">RELATED LINKS</span></span>

[<span data-ttu-id="bf78c-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="bf78c-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="bf78c-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="bf78c-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="bf78c-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="bf78c-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


