---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9cb98b9671f43ddd7acbcc84e8473a12da00f405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430636"
---
# <span data-ttu-id="7fec0-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="7fec0-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="7fec0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fec0-102">SYNOPSIS</span></span>
<span data-ttu-id="7fec0-103">Cria um gateway de gerenciamento de servidor.</span><span class="sxs-lookup"><span data-stu-id="7fec0-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fec0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fec0-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fec0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fec0-105">DESCRIPTION</span></span>
<span data-ttu-id="7fec0-106">O cmdlet **New-AzureRmServerManagementGateway** cria um gateway de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="7fec0-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="7fec0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fec0-107">EXAMPLES</span></span>

## <span data-ttu-id="7fec0-108">OS</span><span class="sxs-lookup"><span data-stu-id="7fec0-108">PARAMETERS</span></span>

### <span data-ttu-id="7fec0-109">-AutoUpgrade</span><span class="sxs-lookup"><span data-stu-id="7fec0-109">-AutoUpgrade</span></span>
<span data-ttu-id="7fec0-110">Indica que o gateway será automaticamente atualizado quando uma nova versão for liberada.</span><span class="sxs-lookup"><span data-stu-id="7fec0-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fec0-111">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="7fec0-111">-GatewayName</span></span>
<span data-ttu-id="7fec0-112">Especifica o nome do gateway que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="7fec0-112">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fec0-113">-Local</span><span class="sxs-lookup"><span data-stu-id="7fec0-113">-Location</span></span>
<span data-ttu-id="7fec0-114">Especifica o local no qual criar o gateway.</span><span class="sxs-lookup"><span data-stu-id="7fec0-114">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fec0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fec0-115">-ResourceGroupName</span></span>
<span data-ttu-id="7fec0-116">Especifica o nome do grupo de recursos no qual esse cmdlet cria o gateway.</span><span class="sxs-lookup"><span data-stu-id="7fec0-116">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fec0-117">-Marcas</span><span class="sxs-lookup"><span data-stu-id="7fec0-117">-Tags</span></span>
<span data-ttu-id="7fec0-118">Especifica marcas como pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="7fec0-118">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="7fec0-119">Você pode usar marcas para identificar um gateway de outros recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7fec0-119">You can use tags to identify a Gateway from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fec0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fec0-120">-DefaultProfile</span></span>
<span data-ttu-id="7fec0-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fec0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fec0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fec0-122">CommonParameters</span></span>
<span data-ttu-id="7fec0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fec0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fec0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fec0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fec0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fec0-125">INPUTS</span></span>

## <span data-ttu-id="7fec0-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fec0-126">OUTPUTS</span></span>

### <span data-ttu-id="7fec0-127">Microsoft. Azure. Commands. ServerManagement. Model. gateway</span><span class="sxs-lookup"><span data-stu-id="7fec0-127">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="7fec0-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fec0-128">NOTES</span></span>

## <span data-ttu-id="7fec0-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fec0-129">RELATED LINKS</span></span>

[<span data-ttu-id="7fec0-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="7fec0-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="7fec0-131">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="7fec0-131">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


