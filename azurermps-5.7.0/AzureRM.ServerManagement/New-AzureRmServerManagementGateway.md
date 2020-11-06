---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: f73d53fc3031fc72be950547e5b9c2b93a9a0079
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602358"
---
# <span data-ttu-id="32939-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="32939-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="32939-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32939-102">SYNOPSIS</span></span>
<span data-ttu-id="32939-103">Cria um gateway de gerenciamento de servidor.</span><span class="sxs-lookup"><span data-stu-id="32939-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32939-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32939-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32939-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32939-105">DESCRIPTION</span></span>
<span data-ttu-id="32939-106">O cmdlet **New-AzureRmServerManagementGateway** cria um gateway de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="32939-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="32939-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32939-107">EXAMPLES</span></span>

## <span data-ttu-id="32939-108">OS</span><span class="sxs-lookup"><span data-stu-id="32939-108">PARAMETERS</span></span>

### <span data-ttu-id="32939-109">-AutoUpgrade</span><span class="sxs-lookup"><span data-stu-id="32939-109">-AutoUpgrade</span></span>
<span data-ttu-id="32939-110">Indica que o gateway será automaticamente atualizado quando uma nova versão for liberada.</span><span class="sxs-lookup"><span data-stu-id="32939-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32939-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32939-111">-DefaultProfile</span></span>
<span data-ttu-id="32939-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32939-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32939-113">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="32939-113">-GatewayName</span></span>
<span data-ttu-id="32939-114">Especifica o nome do gateway que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="32939-114">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32939-115">-Local</span><span class="sxs-lookup"><span data-stu-id="32939-115">-Location</span></span>
<span data-ttu-id="32939-116">Especifica o local no qual criar o gateway.</span><span class="sxs-lookup"><span data-stu-id="32939-116">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32939-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32939-117">-ResourceGroupName</span></span>
<span data-ttu-id="32939-118">Especifica o nome do grupo de recursos no qual esse cmdlet cria o gateway.</span><span class="sxs-lookup"><span data-stu-id="32939-118">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32939-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="32939-119">-Tag</span></span>
<span data-ttu-id="32939-120">Pares de chave/valor associados ao gateway.</span><span class="sxs-lookup"><span data-stu-id="32939-120">Key/value pairs associated with the gateway.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32939-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32939-121">CommonParameters</span></span>
<span data-ttu-id="32939-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32939-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32939-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32939-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32939-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32939-124">INPUTS</span></span>

### <span data-ttu-id="32939-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="32939-125">None</span></span>
<span data-ttu-id="32939-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="32939-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="32939-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32939-127">OUTPUTS</span></span>

### <span data-ttu-id="32939-128">Microsoft. Azure. Commands. ServerManagement. Model. gateway</span><span class="sxs-lookup"><span data-stu-id="32939-128">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="32939-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32939-129">NOTES</span></span>

## <span data-ttu-id="32939-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32939-130">RELATED LINKS</span></span>

[<span data-ttu-id="32939-131">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="32939-131">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="32939-132">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="32939-132">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


