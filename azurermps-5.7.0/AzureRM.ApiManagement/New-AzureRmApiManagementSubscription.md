---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 08685a84817f55e030a62b0b98ddc35be9f05843
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430545"
---
# <span data-ttu-id="c7c3d-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c7c3d-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="c7c3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c3d-103">Cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7c3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7c3d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7c3d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="c7c3d-106">O cmdlet **New-AzureRmApiManagementSubscription** cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="c7c3d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="c7c3d-108">Exemplo 1: assinar um usuário para um produto</span><span class="sxs-lookup"><span data-stu-id="c7c3d-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="c7c3d-109">Esse comando assina um usuário existente para um produto.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="c7c3d-110">OS</span><span class="sxs-lookup"><span data-stu-id="c7c3d-110">PARAMETERS</span></span>

### <span data-ttu-id="c7c3d-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c7c3d-111">-Context</span></span>
<span data-ttu-id="c7c3d-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c7c3d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c7c3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c3d-113">-DefaultProfile</span></span>
<span data-ttu-id="c7c3d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="c7c3d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7c3d-115">-Name</span></span>
<span data-ttu-id="c7c3d-116">Especifica o nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="c7c3d-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c7c3d-117">-PrimaryKey</span></span>
<span data-ttu-id="c7c3d-118">Especifica a chave primária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="c7c3d-119">Se esse parâmetro não for especificado, a chave será gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="c7c3d-120">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c7c3d-121">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c7c3d-121">-ProductId</span></span>
<span data-ttu-id="c7c3d-122">Especifica a ID do produto a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="c7c3d-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="c7c3d-123">-SecondaryKey</span></span>
<span data-ttu-id="c7c3d-124">Especifica a chave secundária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="c7c3d-125">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="c7c3d-126">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c7c3d-127">-Estado</span><span class="sxs-lookup"><span data-stu-id="c7c3d-127">-State</span></span>
<span data-ttu-id="c7c3d-128">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-128">Specifies the subscription state.</span></span>
<span data-ttu-id="c7c3d-129">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-129">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7c3d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7c3d-130">-SubscriptionId</span></span>
<span data-ttu-id="c7c3d-131">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="c7c3d-132">Esse parâmetro é gerado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="c7c3d-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="c7c3d-133">-UserId</span></span>
<span data-ttu-id="c7c3d-134">Especifica a identificação do Assinante.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="c7c3d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c3d-135">CommonParameters</span></span>
<span data-ttu-id="c7c3d-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c3d-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c3d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c3d-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7c3d-138">INPUTS</span></span>

### <span data-ttu-id="c7c3d-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c7c3d-139">None</span></span>
<span data-ttu-id="c7c3d-140">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7c3d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7c3d-141">OUTPUTS</span></span>

### <span data-ttu-id="c7c3d-142">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c7c3d-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="c7c3d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7c3d-143">NOTES</span></span>

## <span data-ttu-id="c7c3d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7c3d-144">RELATED LINKS</span></span>

[<span data-ttu-id="c7c3d-145">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c7c3d-145">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c7c3d-146">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c7c3d-146">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c7c3d-147">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c7c3d-147">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


