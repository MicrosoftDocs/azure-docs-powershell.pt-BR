---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F5EC8E00-E504-436A-96FF-4E886579AEA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b72fcfac0b000a8fcfc11dbab6961460cb25b8b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946415"
---
# <span data-ttu-id="6fa8f-101">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="6fa8f-101">Set-AzureStoreAddOn</span></span>

## <span data-ttu-id="6fa8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fa8f-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa8f-103">Atualiza uma instância de complemento existente.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-103">Updates an existing add-on instance.</span></span>

## <span data-ttu-id="6fa8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fa8f-104">SYNTAX</span></span>

```
Set-AzureStoreAddOn -Name <String> -Plan <String> [-PromotionCode <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6fa8f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fa8f-105">DESCRIPTION</span></span>
<span data-ttu-id="6fa8f-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6fa8f-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6fa8f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6fa8f-108">Este cmdlet atualiza uma instância de complemento existente da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-108">This cmdlet updates an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="6fa8f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fa8f-109">EXAMPLES</span></span>

### <span data-ttu-id="6fa8f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6fa8f-110">Example 1</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId
```

<span data-ttu-id="6fa8f-111">Este exemplo atualiza um complemento com uma nova ID de plano.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-111">This example updates an add-on with a new plan ID.</span></span>

### <span data-ttu-id="6fa8f-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6fa8f-112">Example 2</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId MyPromoCode
```

<span data-ttu-id="6fa8f-113">Este exemplo atualiza um complemento com uma nova ID de plano e código promocional.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-113">This example updates an add-on with a new plan ID and promotional code.</span></span>

## <span data-ttu-id="6fa8f-114">OS</span><span class="sxs-lookup"><span data-stu-id="6fa8f-114">PARAMETERS</span></span>

### <span data-ttu-id="6fa8f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fa8f-115">-Name</span></span>
<span data-ttu-id="6fa8f-116">Especifica o nome da instância do complemento.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-116">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="6fa8f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fa8f-117">-PassThru</span></span>
<span data-ttu-id="6fa8f-118">Se especificado, o cmdlet retornará true se o comando for bem-sucedido e falso se falhar.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-118">If specified, the cmdlet returns true if the command succeeds and false if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa8f-119">-Plano</span><span class="sxs-lookup"><span data-stu-id="6fa8f-119">-Plan</span></span>
<span data-ttu-id="6fa8f-120">Especifica a ID do plano.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-120">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="6fa8f-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6fa8f-121">-Profile</span></span>
<span data-ttu-id="6fa8f-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6fa8f-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6fa8f-124">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="6fa8f-124">-PromotionCode</span></span>
<span data-ttu-id="6fa8f-125">Especifica o código promocional.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-125">Specifies the promotional code.</span></span>

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

### <span data-ttu-id="6fa8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa8f-126">CommonParameters</span></span>
<span data-ttu-id="6fa8f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fa8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa8f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fa8f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa8f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fa8f-129">INPUTS</span></span>

## <span data-ttu-id="6fa8f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fa8f-130">OUTPUTS</span></span>

## <span data-ttu-id="6fa8f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fa8f-131">NOTES</span></span>

## <span data-ttu-id="6fa8f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fa8f-132">RELATED LINKS</span></span>

[<span data-ttu-id="6fa8f-133">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="6fa8f-133">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="6fa8f-134">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="6fa8f-134">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="6fa8f-135">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="6fa8f-135">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)


