---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 2600f8f4039e0d719df2f393ffa16d42a712634a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426506"
---
# <span data-ttu-id="ea433-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ea433-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="ea433-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea433-102">SYNOPSIS</span></span>
<span data-ttu-id="ea433-103">Cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="ea433-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea433-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea433-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea433-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea433-105">DESCRIPTION</span></span>
<span data-ttu-id="ea433-106">O cmdlet **New-AzureRmApiManagementSubscription** cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="ea433-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="ea433-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea433-107">EXAMPLES</span></span>

### <span data-ttu-id="ea433-108">Exemplo 1: assinar um usuário para um produto</span><span class="sxs-lookup"><span data-stu-id="ea433-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="ea433-109">Esse comando assina um usuário existente para um produto.</span><span class="sxs-lookup"><span data-stu-id="ea433-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="ea433-110">OS</span><span class="sxs-lookup"><span data-stu-id="ea433-110">PARAMETERS</span></span>

### <span data-ttu-id="ea433-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ea433-111">-Context</span></span>
<span data-ttu-id="ea433-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ea433-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ea433-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea433-113">-DefaultProfile</span></span>
<span data-ttu-id="ea433-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea433-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea433-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea433-115">-Name</span></span>
<span data-ttu-id="ea433-116">Especifica o nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ea433-116">Specifies the subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea433-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ea433-117">-PrimaryKey</span></span>
<span data-ttu-id="ea433-118">Especifica a chave primária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ea433-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="ea433-119">Se esse parâmetro não for especificado, a chave será gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ea433-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="ea433-120">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="ea433-120">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea433-121">-ProductId</span><span class="sxs-lookup"><span data-stu-id="ea433-121">-ProductId</span></span>
<span data-ttu-id="ea433-122">Especifica a ID do produto a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="ea433-122">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea433-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ea433-123">-SecondaryKey</span></span>
<span data-ttu-id="ea433-124">Especifica a chave secundária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ea433-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="ea433-125">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="ea433-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="ea433-126">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="ea433-126">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea433-127">-Estado</span><span class="sxs-lookup"><span data-stu-id="ea433-127">-State</span></span>
<span data-ttu-id="ea433-128">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ea433-128">Specifies the subscription state.</span></span>
<span data-ttu-id="ea433-129">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="ea433-129">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea433-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea433-130">-SubscriptionId</span></span>
<span data-ttu-id="ea433-131">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ea433-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="ea433-132">Esse parâmetro é gerado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="ea433-132">This parameter is generated if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea433-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="ea433-133">-UserId</span></span>
<span data-ttu-id="ea433-134">Especifica a identificação do Assinante.</span><span class="sxs-lookup"><span data-stu-id="ea433-134">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea433-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea433-135">CommonParameters</span></span>
<span data-ttu-id="ea433-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea433-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea433-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea433-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea433-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea433-138">INPUTS</span></span>

### <span data-ttu-id="ea433-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ea433-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ea433-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ea433-140">System.String</span></span>

### <span data-ttu-id="ea433-141">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementSubscriptionState, Microsoft. Azure. Commands. ApiManagement. onmanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ea433-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ea433-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea433-142">OUTPUTS</span></span>

### <span data-ttu-id="ea433-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ea433-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="ea433-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea433-144">NOTES</span></span>

## <span data-ttu-id="ea433-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea433-145">RELATED LINKS</span></span>

[<span data-ttu-id="ea433-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ea433-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="ea433-147">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ea433-147">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="ea433-148">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ea433-148">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


