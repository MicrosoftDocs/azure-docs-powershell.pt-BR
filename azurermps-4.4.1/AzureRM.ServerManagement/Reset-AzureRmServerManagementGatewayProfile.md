---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 9ce8dc1faf1a762a847da5eb87fb28b510308054
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603318"
---
# <span data-ttu-id="7a5dd-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7a5dd-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="7a5dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a5dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5dd-103">Redefine o perfil de um gateway de gerenciamento de servidor.</span><span class="sxs-lookup"><span data-stu-id="7a5dd-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a5dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a5dd-104">SYNTAX</span></span>

### <span data-ttu-id="7a5dd-105">ByName</span><span class="sxs-lookup"><span data-stu-id="7a5dd-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a5dd-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="7a5dd-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a5dd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a5dd-107">DESCRIPTION</span></span>
<span data-ttu-id="7a5dd-108">O cmdlet **Reset-AzureRmServerManagementGatewayProfile** redefine o perfil para um gateway de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a5dd-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="7a5dd-109">Você precisará usar o cmdlet Save-AzureRmServerManagementGatewayProfile para baixar o perfil e, em seguida, o cmdlet Install-AzureRmServerManagementGatewayProfile para salvá-lo depois de redefinir o perfil.</span><span class="sxs-lookup"><span data-stu-id="7a5dd-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="7a5dd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a5dd-110">EXAMPLES</span></span>

## <span data-ttu-id="7a5dd-111">OS</span><span class="sxs-lookup"><span data-stu-id="7a5dd-111">PARAMETERS</span></span>

### <span data-ttu-id="7a5dd-112">-Gateway</span><span class="sxs-lookup"><span data-stu-id="7a5dd-112">-Gateway</span></span>
<span data-ttu-id="7a5dd-113">Especifica o gateway para o qual o cmdlet redefine o perfil.</span><span class="sxs-lookup"><span data-stu-id="7a5dd-113">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="7a5dd-114">Pode ser especificado em vez de ResourceGoupName e GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="7a5dd-114">May be specified instead of ResourceGoupName and GatewayName</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a5dd-115">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="7a5dd-115">-GatewayName</span></span>
<span data-ttu-id="7a5dd-116">Especifica o nome do gateway para o qual o cmdlet redefine o perfil.</span><span class="sxs-lookup"><span data-stu-id="7a5dd-116">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a5dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a5dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a5dd-118">Especifica o nome do grupo de recursos ao qual o gateway pertence.</span><span class="sxs-lookup"><span data-stu-id="7a5dd-118">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a5dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5dd-119">-DefaultProfile</span></span>
<span data-ttu-id="7a5dd-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a5dd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a5dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5dd-121">CommonParameters</span></span>
<span data-ttu-id="7a5dd-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a5dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5dd-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a5dd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5dd-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a5dd-124">INPUTS</span></span>

### <span data-ttu-id="7a5dd-125">Gateway</span><span class="sxs-lookup"><span data-stu-id="7a5dd-125">Gateway</span></span>
<span data-ttu-id="7a5dd-126">O parâmetro ' gateway ' aceita o valor do tipo ' gateway ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="7a5dd-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="7a5dd-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a5dd-127">OUTPUTS</span></span>

## <span data-ttu-id="7a5dd-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a5dd-128">NOTES</span></span>

## <span data-ttu-id="7a5dd-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a5dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="7a5dd-130">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7a5dd-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="7a5dd-131">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7a5dd-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


