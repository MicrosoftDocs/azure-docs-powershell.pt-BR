---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 360bf469f5496d837d12fb6cd4fa8dba9cefd724
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440231"
---
# <span data-ttu-id="874fe-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="874fe-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="874fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="874fe-102">SYNOPSIS</span></span>
<span data-ttu-id="874fe-103">Cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="874fe-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="874fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="874fe-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="874fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="874fe-105">DESCRIPTION</span></span>
<span data-ttu-id="874fe-106">O cmdlet **New-AzureRmApiManagementSubscription** cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="874fe-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="874fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="874fe-107">EXAMPLES</span></span>

### <span data-ttu-id="874fe-108">Exemplo 1: assinar um usuário para um produto</span><span class="sxs-lookup"><span data-stu-id="874fe-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="874fe-109">Esse comando assina um usuário existente para um produto.</span><span class="sxs-lookup"><span data-stu-id="874fe-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="874fe-110">OS</span><span class="sxs-lookup"><span data-stu-id="874fe-110">PARAMETERS</span></span>

### <span data-ttu-id="874fe-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="874fe-111">-Context</span></span>
<span data-ttu-id="874fe-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="874fe-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="874fe-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="874fe-113">-Name</span></span>
<span data-ttu-id="874fe-114">Especifica o nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="874fe-114">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="874fe-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="874fe-115">-PrimaryKey</span></span>
<span data-ttu-id="874fe-116">Especifica a chave primária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="874fe-116">Specifies the subscription primary key.</span></span>
<span data-ttu-id="874fe-117">Se esse parâmetro não for especificado, a chave será gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="874fe-117">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="874fe-118">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="874fe-118">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="874fe-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="874fe-119">-ProductId</span></span>
<span data-ttu-id="874fe-120">Especifica a ID do produto a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="874fe-120">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="874fe-121">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="874fe-121">-SecondaryKey</span></span>
<span data-ttu-id="874fe-122">Especifica a chave secundária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="874fe-122">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="874fe-123">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="874fe-123">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="874fe-124">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="874fe-124">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="874fe-125">-Estado</span><span class="sxs-lookup"><span data-stu-id="874fe-125">-State</span></span>
<span data-ttu-id="874fe-126">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="874fe-126">Specifies the subscription state.</span></span>
<span data-ttu-id="874fe-127">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="874fe-127">The default value is $Null.</span></span>

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

### <span data-ttu-id="874fe-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="874fe-128">-SubscriptionId</span></span>
<span data-ttu-id="874fe-129">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="874fe-129">Specifies the subscription ID.</span></span>
<span data-ttu-id="874fe-130">Esse parâmetro é gerado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="874fe-130">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="874fe-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="874fe-131">-UserId</span></span>
<span data-ttu-id="874fe-132">Especifica a identificação do Assinante.</span><span class="sxs-lookup"><span data-stu-id="874fe-132">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="874fe-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="874fe-133">-DefaultProfile</span></span>
<span data-ttu-id="874fe-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="874fe-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="874fe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="874fe-135">CommonParameters</span></span>
<span data-ttu-id="874fe-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="874fe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="874fe-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="874fe-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="874fe-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="874fe-138">INPUTS</span></span>

## <span data-ttu-id="874fe-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="874fe-139">OUTPUTS</span></span>

### <span data-ttu-id="874fe-140">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="874fe-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="874fe-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="874fe-141">NOTES</span></span>

## <span data-ttu-id="874fe-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="874fe-142">RELATED LINKS</span></span>

[<span data-ttu-id="874fe-143">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="874fe-143">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="874fe-144">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="874fe-144">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="874fe-145">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="874fe-145">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


