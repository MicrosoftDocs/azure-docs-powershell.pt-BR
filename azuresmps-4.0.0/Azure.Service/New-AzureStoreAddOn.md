---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 793037C4-8FE5-4799-B59B-94C1605D9F4E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 593ea36e90635472db1f8568254657f782bd1200
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946201"
---
# <span data-ttu-id="20830-101">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="20830-101">New-AzureStoreAddOn</span></span>

## <span data-ttu-id="20830-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20830-102">SYNOPSIS</span></span>
<span data-ttu-id="20830-103">Compra uma nova instância de complemento.</span><span class="sxs-lookup"><span data-stu-id="20830-103">Buys a new add-on instance.</span></span>

## <span data-ttu-id="20830-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20830-104">SYNTAX</span></span>

```
New-AzureStoreAddOn -Name <String> -AddOn <String> -Plan <String> -Location <String> [-PromotionCode <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="20830-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20830-105">DESCRIPTION</span></span>
<span data-ttu-id="20830-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="20830-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="20830-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="20830-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="20830-108">Compra uma nova instância de complemento da Azure Store.</span><span class="sxs-lookup"><span data-stu-id="20830-108">Buys a new add-on instance from the Azure Store.</span></span>

## <span data-ttu-id="20830-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20830-109">EXAMPLES</span></span>

### <span data-ttu-id="20830-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20830-110">Example 1</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US"
```

<span data-ttu-id="20830-111">Este exemplo compra um complemento chamado myaddon com um PlanID na localização dos EUA do oeste.</span><span class="sxs-lookup"><span data-stu-id="20830-111">This example buys an add-on named MyAddOn with a PlanId in West US location.</span></span>

### <span data-ttu-id="20830-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="20830-112">Example 2</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US" -PromotionCode MyPromoCode
```

<span data-ttu-id="20830-113">Este exemplo usa um código promocional para comprar um complemento.</span><span class="sxs-lookup"><span data-stu-id="20830-113">This example uses a promotional code to buy an add-on.</span></span>

## <span data-ttu-id="20830-114">OS</span><span class="sxs-lookup"><span data-stu-id="20830-114">PARAMETERS</span></span>

### <span data-ttu-id="20830-115">-AddOn</span><span class="sxs-lookup"><span data-stu-id="20830-115">-AddOn</span></span>
<span data-ttu-id="20830-116">Especifica a ID do complemento.</span><span class="sxs-lookup"><span data-stu-id="20830-116">Specifies the add-on ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20830-117">-Local</span><span class="sxs-lookup"><span data-stu-id="20830-117">-Location</span></span>
<span data-ttu-id="20830-118">Especifica o local da instância do complemento.</span><span class="sxs-lookup"><span data-stu-id="20830-118">Specifies the add-on instance location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20830-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="20830-119">-Name</span></span>
<span data-ttu-id="20830-120">Especifica o nome da instância do complemento.</span><span class="sxs-lookup"><span data-stu-id="20830-120">Specifies the name of the add-on instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20830-121">-Plano</span><span class="sxs-lookup"><span data-stu-id="20830-121">-Plan</span></span>
<span data-ttu-id="20830-122">Especifica a ID do plano.</span><span class="sxs-lookup"><span data-stu-id="20830-122">Specifies the plan ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20830-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="20830-123">-Profile</span></span>
<span data-ttu-id="20830-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="20830-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20830-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="20830-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20830-126">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="20830-126">-PromotionCode</span></span>
<span data-ttu-id="20830-127">Especifica um código promocional para aplicar à compra.</span><span class="sxs-lookup"><span data-stu-id="20830-127">Specifies a promotion code to apply to the purchase.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20830-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20830-128">CommonParameters</span></span>
<span data-ttu-id="20830-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20830-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20830-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20830-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20830-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20830-131">INPUTS</span></span>

## <span data-ttu-id="20830-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20830-132">OUTPUTS</span></span>

## <span data-ttu-id="20830-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20830-133">NOTES</span></span>

## <span data-ttu-id="20830-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20830-134">RELATED LINKS</span></span>

[<span data-ttu-id="20830-135">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="20830-135">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="20830-136">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="20830-136">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="20830-137">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="20830-137">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


