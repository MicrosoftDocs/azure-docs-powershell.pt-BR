---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426848"
---
# <span data-ttu-id="a455d-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a455d-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="a455d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a455d-102">SYNOPSIS</span></span>
<span data-ttu-id="a455d-103">Obtém assinaturas.</span><span class="sxs-lookup"><span data-stu-id="a455d-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a455d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a455d-104">SYNTAX</span></span>

### <span data-ttu-id="a455d-105">GetAllSubscriptions (padrão)</span><span class="sxs-lookup"><span data-stu-id="a455d-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a455d-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a455d-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a455d-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="a455d-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a455d-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="a455d-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a455d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a455d-109">DESCRIPTION</span></span>
<span data-ttu-id="a455d-110">O cmdlet **Get-AzureRmApiManagementSubscription** Obtém uma assinatura especificada, ou todas as assinaturas, se nenhuma assinatura for especificada.</span><span class="sxs-lookup"><span data-stu-id="a455d-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="a455d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a455d-111">EXAMPLES</span></span>

### <span data-ttu-id="a455d-112">Exemplo 1: obter todas as assinaturas</span><span class="sxs-lookup"><span data-stu-id="a455d-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="a455d-113">Este comando obtém todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="a455d-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="a455d-114">Exemplo 2: obter uma assinatura com uma ID especificada</span><span class="sxs-lookup"><span data-stu-id="a455d-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="a455d-115">Este comando obtém uma assinatura por ID.</span><span class="sxs-lookup"><span data-stu-id="a455d-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="a455d-116">Exemplo 3: obter todas as assinaturas de um usuário</span><span class="sxs-lookup"><span data-stu-id="a455d-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="a455d-117">Este comando obtém as assinaturas de um usuário.</span><span class="sxs-lookup"><span data-stu-id="a455d-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="a455d-118">Exemplo 4: obter todas as assinaturas de um produto</span><span class="sxs-lookup"><span data-stu-id="a455d-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="a455d-119">Este comando obtém todas as assinaturas do produto.</span><span class="sxs-lookup"><span data-stu-id="a455d-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="a455d-120">OS</span><span class="sxs-lookup"><span data-stu-id="a455d-120">PARAMETERS</span></span>

### <span data-ttu-id="a455d-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a455d-121">-Context</span></span>
<span data-ttu-id="a455d-122">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a455d-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a455d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a455d-123">-DefaultProfile</span></span>
<span data-ttu-id="a455d-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a455d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a455d-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a455d-125">-ProductId</span></span>
<span data-ttu-id="a455d-126">Especifica um identificador de produto.</span><span class="sxs-lookup"><span data-stu-id="a455d-126">Specifies a product identifier.</span></span>
<span data-ttu-id="a455d-127">Se especificado, esse cmdlet encontra todas as assinaturas pelo identificador do produto.</span><span class="sxs-lookup"><span data-stu-id="a455d-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a455d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a455d-128">-SubscriptionId</span></span>
<span data-ttu-id="a455d-129">Especifica um identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a455d-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="a455d-130">Se especificado, esse cmdlet localiza a assinatura pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="a455d-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetBySubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a455d-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="a455d-131">-UserId</span></span>
<span data-ttu-id="a455d-132">Especifica um identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="a455d-132">Specifies a user identifier.</span></span>
<span data-ttu-id="a455d-133">Se especificado, esse cmdlet encontra todas as assinaturas pelo identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="a455d-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a455d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a455d-134">CommonParameters</span></span>
<span data-ttu-id="a455d-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a455d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a455d-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a455d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a455d-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a455d-137">INPUTS</span></span>

### <span data-ttu-id="a455d-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a455d-138">None</span></span>
<span data-ttu-id="a455d-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a455d-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a455d-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a455d-140">OUTPUTS</span></span>

### <span data-ttu-id="a455d-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a455d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>
<span data-ttu-id="a455d-142">O detalhe da assinatura no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a455d-142">The detail of the subscription in the API Management service.</span></span>

### <span data-ttu-id="a455d-143">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="a455d-143">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>
<span data-ttu-id="a455d-144">A lista de assinaturas no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a455d-144">The list of subscription in API Management service.</span></span>

## <span data-ttu-id="a455d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a455d-145">NOTES</span></span>

## <span data-ttu-id="a455d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a455d-146">RELATED LINKS</span></span>

[<span data-ttu-id="a455d-147">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a455d-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="a455d-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a455d-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="a455d-149">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a455d-149">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


