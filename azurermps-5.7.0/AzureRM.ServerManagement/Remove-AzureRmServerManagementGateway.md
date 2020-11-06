---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 53bf195bf801b4746f0ea958949f1683c8ca3d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609486"
---
# <span data-ttu-id="a6ece-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a6ece-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="a6ece-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6ece-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ece-103">Remove um gateway de gerenciamento de servidor.</span><span class="sxs-lookup"><span data-stu-id="a6ece-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6ece-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6ece-104">SYNTAX</span></span>

### <span data-ttu-id="a6ece-105">ByName</span><span class="sxs-lookup"><span data-stu-id="a6ece-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6ece-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a6ece-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6ece-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6ece-107">DESCRIPTION</span></span>
<span data-ttu-id="a6ece-108">O cmdlet **Remove-AzureRmServerManagementGateway** remove um gateway de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ece-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="a6ece-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6ece-109">EXAMPLES</span></span>

## <span data-ttu-id="a6ece-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6ece-110">PARAMETERS</span></span>

### <span data-ttu-id="a6ece-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ece-111">-DefaultProfile</span></span>
<span data-ttu-id="a6ece-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ece-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6ece-113">-Gateway</span><span class="sxs-lookup"><span data-stu-id="a6ece-113">-Gateway</span></span>
<span data-ttu-id="a6ece-114">Especifica o gateway que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="a6ece-114">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="a6ece-115">Esse parâmetro pode ser usado em vez dos parâmetros *ResourceGroupName* e *GATEWAYNAME* .</span><span class="sxs-lookup"><span data-stu-id="a6ece-115">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ece-116">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="a6ece-116">-GatewayName</span></span>
<span data-ttu-id="a6ece-117">Especifica o nome do gateway que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="a6ece-117">Specifies the name of the gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ece-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ece-118">-ResourceGroupName</span></span>
<span data-ttu-id="a6ece-119">Especifica o nome do grupo de recursos no qual o gateway pertence.</span><span class="sxs-lookup"><span data-stu-id="a6ece-119">Specifies the name of the resource group in that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ece-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ece-120">CommonParameters</span></span>
<span data-ttu-id="a6ece-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6ece-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ece-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6ece-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ece-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6ece-123">INPUTS</span></span>

### <span data-ttu-id="a6ece-124">Gateway</span><span class="sxs-lookup"><span data-stu-id="a6ece-124">Gateway</span></span>
<span data-ttu-id="a6ece-125">O parâmetro ' gateway ' aceita o valor do tipo ' gateway ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a6ece-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="a6ece-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6ece-126">OUTPUTS</span></span>

## <span data-ttu-id="a6ece-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6ece-127">NOTES</span></span>
* <span data-ttu-id="a6ece-128">Todos os nós do gateway devem ser removidos antes de usar este cmdlet; caso contrário, esse cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="a6ece-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="a6ece-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6ece-129">RELATED LINKS</span></span>

[<span data-ttu-id="a6ece-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a6ece-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="a6ece-131">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="a6ece-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


