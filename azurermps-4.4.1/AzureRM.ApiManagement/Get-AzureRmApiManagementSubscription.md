---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440244"
---
# <span data-ttu-id="409da-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="409da-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="409da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="409da-102">SYNOPSIS</span></span>
<span data-ttu-id="409da-103">Obtém assinaturas.</span><span class="sxs-lookup"><span data-stu-id="409da-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="409da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="409da-104">SYNTAX</span></span>

### <span data-ttu-id="409da-105">Obter todas as assinaturas (padrão)</span><span class="sxs-lookup"><span data-stu-id="409da-105">Get all subscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409da-106">Obter por ID do subsctiption</span><span class="sxs-lookup"><span data-stu-id="409da-106">Get by subsctiption ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409da-107">Obter por ID do usuário</span><span class="sxs-lookup"><span data-stu-id="409da-107">Get by user ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409da-108">Obter por ID do produto</span><span class="sxs-lookup"><span data-stu-id="409da-108">Get by product ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="409da-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="409da-109">DESCRIPTION</span></span>
<span data-ttu-id="409da-110">O cmdlet **Get-AzureRmApiManagementSubscription** Obtém uma assinatura especificada, ou todas as assinaturas, se nenhuma assinatura for especificada.</span><span class="sxs-lookup"><span data-stu-id="409da-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="409da-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="409da-111">EXAMPLES</span></span>

### <span data-ttu-id="409da-112">Exemplo 1: obter todas as assinaturas</span><span class="sxs-lookup"><span data-stu-id="409da-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="409da-113">Este comando obtém todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="409da-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="409da-114">Exemplo 2: obter uma assinatura com uma ID especificada</span><span class="sxs-lookup"><span data-stu-id="409da-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="409da-115">Este comando obtém uma assinatura por ID.</span><span class="sxs-lookup"><span data-stu-id="409da-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="409da-116">Exemplo 3: obter todas as assinaturas de um usuário</span><span class="sxs-lookup"><span data-stu-id="409da-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="409da-117">Este comando obtém as assinaturas de um usuário.</span><span class="sxs-lookup"><span data-stu-id="409da-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="409da-118">Exemplo 4: obter todas as assinaturas de um produto</span><span class="sxs-lookup"><span data-stu-id="409da-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="409da-119">Este comando obtém todas as assinaturas do produto.</span><span class="sxs-lookup"><span data-stu-id="409da-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="409da-120">OS</span><span class="sxs-lookup"><span data-stu-id="409da-120">PARAMETERS</span></span>

### <span data-ttu-id="409da-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="409da-121">-Context</span></span>
<span data-ttu-id="409da-122">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="409da-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="409da-123">-ProductId</span><span class="sxs-lookup"><span data-stu-id="409da-123">-ProductId</span></span>
<span data-ttu-id="409da-124">Especifica um identificador de produto.</span><span class="sxs-lookup"><span data-stu-id="409da-124">Specifies a product identifier.</span></span>
<span data-ttu-id="409da-125">Se especificado, esse cmdlet encontra todas as assinaturas pelo identificador do produto.</span><span class="sxs-lookup"><span data-stu-id="409da-125">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="409da-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="409da-126">-SubscriptionId</span></span>
<span data-ttu-id="409da-127">Especifica um identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="409da-127">Specifies a subscription identifier.</span></span>
<span data-ttu-id="409da-128">Se especificado, esse cmdlet localiza a assinatura pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="409da-128">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="409da-129">-UserId</span><span class="sxs-lookup"><span data-stu-id="409da-129">-UserId</span></span>
<span data-ttu-id="409da-130">Especifica um identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="409da-130">Specifies a user identifier.</span></span>
<span data-ttu-id="409da-131">Se especificado, esse cmdlet encontra todas as assinaturas pelo identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="409da-131">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="409da-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="409da-132">-DefaultProfile</span></span>
<span data-ttu-id="409da-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="409da-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409da-134">CommonParameters</span></span>
<span data-ttu-id="409da-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="409da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409da-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="409da-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409da-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="409da-137">INPUTS</span></span>

## <span data-ttu-id="409da-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="409da-138">OUTPUTS</span></span>

### <span data-ttu-id="409da-139">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="409da-139">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>

## <span data-ttu-id="409da-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="409da-140">NOTES</span></span>

## <span data-ttu-id="409da-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="409da-141">RELATED LINKS</span></span>

[<span data-ttu-id="409da-142">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="409da-142">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="409da-143">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="409da-143">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="409da-144">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="409da-144">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


