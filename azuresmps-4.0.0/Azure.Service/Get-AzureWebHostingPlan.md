---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946512"
---
# <span data-ttu-id="aa3ab-101">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="aa3ab-101">Get-AzureWebHostingPlan</span></span>

## <span data-ttu-id="aa3ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3ab-103">Obtém os planos de hospedagem da Web do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-103">Gets Azure web hosting plans in the current subscription.</span></span>

## <span data-ttu-id="aa3ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa3ab-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa3ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa3ab-105">DESCRIPTION</span></span>
<span data-ttu-id="aa3ab-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="aa3ab-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="aa3ab-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="aa3ab-108">O cmdlet **Get-AzureWebHostingPlan** Obtém os planos de hospedagem da Web do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-108">The **Get-AzureWebHostingPlan** cmdlet gets the Azure web hosting plans in the current subscription.</span></span>

<span data-ttu-id="aa3ab-109">Por padrão, **Get-AzureWebHostingPlan** Obtém todos os planos de hospedagem do Azure na assinatura atual e retorna um objeto que fornece informações básicas sobre os planos.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-109">By default, **Get-AzureWebHostingPlan** gets all Azure hosting plans in the current subscription and returns an object that provides basic information about the plans.</span></span>
<span data-ttu-id="aa3ab-110">Quando você usa os parâmetros *espaço* de *nomes e nome* , **Get-AzureWebHostingPlan** retorna um objeto de plano de hospedagem específico.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-110">When you use the *WebSpace* and *Name* parameters, **Get-AzureWebHostingPlan** returns a specific hosting plan object.</span></span>

<span data-ttu-id="aa3ab-111">Para localizar a assinatura atual, use o parâmetro *atual* do cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="aa3ab-111">To find the current subscription, use the *Current* parameter of the **Get-AzureSubscription** cmdlet.</span></span>
<span data-ttu-id="aa3ab-112">Para alterar a assinatura atual, use o cmdlet **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="aa3ab-112">To change the current subscription, use the **Select-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="aa3ab-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa3ab-113">EXAMPLES</span></span>

### <span data-ttu-id="aa3ab-114">Exemplo 1: obter todos os planos de hospedagem na Web em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="aa3ab-114">Example 1: Get all web hosting plans in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

<span data-ttu-id="aa3ab-115">Este comando obtém todos os planos de hospedagem da Web do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-115">This command gets all Azure web hosting plans in the current subscription.</span></span>

### <span data-ttu-id="aa3ab-116">Exemplo 2: obter um plano de hospedagem da Web específico em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="aa3ab-116">Example 2: Get a specific web hosting plan in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

<span data-ttu-id="aa3ab-117">Esse comando obtém o plano de hospedagem na Web chamado Default0 no espaço de nomes westeuropewebspace na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-117">This command gets the web hosting plan named Default0 in the webspace named westeuropewebspace in the current subscription.</span></span>

## <span data-ttu-id="aa3ab-118">OS</span><span class="sxs-lookup"><span data-stu-id="aa3ab-118">PARAMETERS</span></span>

### <span data-ttu-id="aa3ab-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa3ab-119">-Name</span></span>
<span data-ttu-id="aa3ab-120">Especifica o nome de um plano na assinatura.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-120">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="aa3ab-121">Por padrão, esse cmdlet obtém todos os planos na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-121">By default, this cmdlet gets all plans in the current subscription.</span></span>
<span data-ttu-id="aa3ab-122">Esse parâmetro não oferece suporte a caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-122">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="aa3ab-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="aa3ab-123">-Profile</span></span>
<span data-ttu-id="aa3ab-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aa3ab-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aa3ab-126">-Webspacename</span><span class="sxs-lookup"><span data-stu-id="aa3ab-126">-WebSpaceName</span></span>
<span data-ttu-id="aa3ab-127">Especifica o nome de um espaço da Web na assinatura.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-127">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="aa3ab-128">Por padrão, esse cmdlet obtém todos os sites no espaço Web especificado.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-128">By default, this cmdlet gets all websites in the specified webspace.</span></span>
<span data-ttu-id="aa3ab-129">Esse parâmetro não oferece suporte a caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-129">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa3ab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3ab-130">CommonParameters</span></span>
<span data-ttu-id="aa3ab-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3ab-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa3ab-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3ab-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa3ab-133">INPUTS</span></span>

###  
<span data-ttu-id="aa3ab-134">Você pode passar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-134">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="aa3ab-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa3ab-135">OUTPUTS</span></span>

### <span data-ttu-id="aa3ab-136">Microsoft. WindowsAzure. Commands. Utilities. sites. Services. webentities. WebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="aa3ab-136">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.WebHostingPlan</span></span>
<span data-ttu-id="aa3ab-137">Por padrão, **Get-AzureWebHostingPlan** retorna uma matriz de objetos **WebHostingPlan** .</span><span class="sxs-lookup"><span data-stu-id="aa3ab-137">By default, **Get-AzureWebHostingPlan** returns an array of **WebHostingPlan** objects.</span></span>

## <span data-ttu-id="aa3ab-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa3ab-138">NOTES</span></span>

## <span data-ttu-id="aa3ab-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa3ab-139">RELATED LINKS</span></span>

