---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111245"
---
# <span data-ttu-id="682a7-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="682a7-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="682a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="682a7-102">SYNOPSIS</span></span>
<span data-ttu-id="682a7-103">Obtém chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="682a7-103">Gets subscription keys.</span></span>

## <span data-ttu-id="682a7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="682a7-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="682a7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="682a7-105">DESCRIPTION</span></span>
<span data-ttu-id="682a7-106">O cmdlet **Get-AzApiManagementSubscriptionKey** obtém as chaves de uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="682a7-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="682a7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="682a7-107">EXAMPLES</span></span>

### <span data-ttu-id="682a7-108">Exemplo 1: Obter uma chave de assinatura com uma ID especificada</span><span class="sxs-lookup"><span data-stu-id="682a7-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="682a7-109">Este comando obtém uma assinatura por ID.</span><span class="sxs-lookup"><span data-stu-id="682a7-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="682a7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="682a7-110">PARAMETERS</span></span>

### <span data-ttu-id="682a7-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="682a7-111">-Context</span></span>
<span data-ttu-id="682a7-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="682a7-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="682a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="682a7-113">-DefaultProfile</span></span>
<span data-ttu-id="682a7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="682a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="682a7-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="682a7-115">-SubscriptionId</span></span>
<span data-ttu-id="682a7-116">Especifica um identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="682a7-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="682a7-117">Se especificado, esse cmdlet localiza a assinatura pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="682a7-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="682a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="682a7-118">CommonParameters</span></span>
<span data-ttu-id="682a7-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="682a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="682a7-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="682a7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="682a7-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="682a7-121">INPUTS</span></span>

### <span data-ttu-id="682a7-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="682a7-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="682a7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="682a7-123">System.String</span></span>

## <span data-ttu-id="682a7-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="682a7-124">OUTPUTS</span></span>

### <span data-ttu-id="682a7-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="682a7-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="682a7-126">Notas</span><span class="sxs-lookup"><span data-stu-id="682a7-126">NOTES</span></span>

## <span data-ttu-id="682a7-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="682a7-127">RELATED LINKS</span></span>

[<span data-ttu-id="682a7-128">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="682a7-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="682a7-129">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="682a7-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="682a7-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="682a7-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="682a7-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="682a7-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


