---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 885d552f6040d4c88c007a37f839ac030ba671c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595667"
---
# <span data-ttu-id="d8f46-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d8f46-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="d8f46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8f46-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f46-103">Obtém assinaturas.</span><span class="sxs-lookup"><span data-stu-id="d8f46-103">Gets subscriptions.</span></span>

## <span data-ttu-id="d8f46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8f46-104">SYNTAX</span></span>

### <span data-ttu-id="d8f46-105">GetAllSubscriptions (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8f46-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8f46-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8f46-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8f46-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="d8f46-107">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8f46-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="d8f46-108">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f46-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8f46-109">DESCRIPTION</span></span>
<span data-ttu-id="d8f46-110">O cmdlet **Get-AzApiManagementSubscription** Obtém uma assinatura especificada, ou todas as assinaturas, se nenhuma assinatura for especificada.</span><span class="sxs-lookup"><span data-stu-id="d8f46-110">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="d8f46-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8f46-111">EXAMPLES</span></span>

### <span data-ttu-id="d8f46-112">Exemplo 1: obter todas as assinaturas</span><span class="sxs-lookup"><span data-stu-id="d8f46-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="d8f46-113">Este comando obtém todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="d8f46-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="d8f46-114">Exemplo 2: obter uma assinatura com uma ID especificada</span><span class="sxs-lookup"><span data-stu-id="d8f46-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="d8f46-115">Este comando obtém uma assinatura por ID.</span><span class="sxs-lookup"><span data-stu-id="d8f46-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="d8f46-116">Exemplo 3: obter todas as assinaturas de um usuário</span><span class="sxs-lookup"><span data-stu-id="d8f46-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="d8f46-117">Este comando obtém as assinaturas de um usuário.</span><span class="sxs-lookup"><span data-stu-id="d8f46-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="d8f46-118">Exemplo 4: obter todas as assinaturas de um produto</span><span class="sxs-lookup"><span data-stu-id="d8f46-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="d8f46-119">Este comando obtém todas as assinaturas do produto.</span><span class="sxs-lookup"><span data-stu-id="d8f46-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="d8f46-120">OS</span><span class="sxs-lookup"><span data-stu-id="d8f46-120">PARAMETERS</span></span>

### <span data-ttu-id="d8f46-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d8f46-121">-Context</span></span>
<span data-ttu-id="d8f46-122">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d8f46-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f46-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f46-123">-DefaultProfile</span></span>
<span data-ttu-id="d8f46-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f46-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f46-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d8f46-125">-ProductId</span></span>
<span data-ttu-id="d8f46-126">Especifica um identificador de produto.</span><span class="sxs-lookup"><span data-stu-id="d8f46-126">Specifies a product identifier.</span></span>
<span data-ttu-id="d8f46-127">Se especificado, esse cmdlet encontra todas as assinaturas pelo identificador do produto.</span><span class="sxs-lookup"><span data-stu-id="d8f46-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f46-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8f46-128">-SubscriptionId</span></span>
<span data-ttu-id="d8f46-129">Especifica um identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="d8f46-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="d8f46-130">Se especificado, esse cmdlet localiza a assinatura pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="d8f46-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f46-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="d8f46-131">-UserId</span></span>
<span data-ttu-id="d8f46-132">Especifica um identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="d8f46-132">Specifies a user identifier.</span></span>
<span data-ttu-id="d8f46-133">Se especificado, esse cmdlet encontra todas as assinaturas pelo identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="d8f46-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f46-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f46-134">CommonParameters</span></span>
<span data-ttu-id="d8f46-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f46-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f46-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8f46-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f46-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8f46-137">INPUTS</span></span>

### <span data-ttu-id="d8f46-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d8f46-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d8f46-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d8f46-139">System.String</span></span>

## <span data-ttu-id="d8f46-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8f46-140">OUTPUTS</span></span>

### <span data-ttu-id="d8f46-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d8f46-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="d8f46-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8f46-142">NOTES</span></span>

## <span data-ttu-id="d8f46-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8f46-143">RELATED LINKS</span></span>

[<span data-ttu-id="d8f46-144">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d8f46-144">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="d8f46-145">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d8f46-145">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="d8f46-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d8f46-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


