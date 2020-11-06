---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: f1676d385b23711e71fbec5fb5d9131add4daaf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430749"
---
# <span data-ttu-id="80a4d-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="80a4d-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="80a4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="80a4d-103">Cria uma chave de gateway para um Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="80a4d-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="80a4d-104">Esse cmdlet é preterido e você deve usar **New-AzureRmDataFactoryGatewayAuthKey** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="80a4d-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80a4d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80a4d-105">SYNTAX</span></span>

### <span data-ttu-id="80a4d-106">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="80a4d-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80a4d-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="80a4d-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80a4d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80a4d-108">DESCRIPTION</span></span>
<span data-ttu-id="80a4d-109">O cmdlet **New-AzureRmDataFactoryGatewayKey** cria uma chave de gateway para um gateway de fábrica de dados do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="80a4d-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="80a4d-110">Você registra o gateway com um serviço na nuvem usando essa chave.</span><span class="sxs-lookup"><span data-stu-id="80a4d-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="80a4d-111">Esse cmdlet é preterido e você deve usar **New-AzureRmDataFactoryGatewayAuthKey** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="80a4d-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="80a4d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80a4d-112">EXAMPLES</span></span>

### <span data-ttu-id="80a4d-113">Exemplo 1: criar uma chave de gateway</span><span class="sxs-lookup"><span data-stu-id="80a4d-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="80a4d-114">Esse comando cria uma chave de gateway para o gateway de fábrica de dados chamado ContosoGateway e, em seguida, passa a chave de gateway para o cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="80a4d-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="80a4d-115">Para obter mais informações, digite `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="80a4d-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="80a4d-116">OS</span><span class="sxs-lookup"><span data-stu-id="80a4d-116">PARAMETERS</span></span>

### <span data-ttu-id="80a4d-117">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="80a4d-117">-DataFactory</span></span>
<span data-ttu-id="80a4d-118">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="80a4d-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="80a4d-119">Esse cmdlet cria uma chave de gateway para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="80a4d-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a4d-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="80a4d-120">-DataFactoryName</span></span>
<span data-ttu-id="80a4d-121">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="80a4d-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="80a4d-122">Esse cmdlet cria uma chave de gateway para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="80a4d-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a4d-123">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="80a4d-123">-GatewayName</span></span>
<span data-ttu-id="80a4d-124">Especifica o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="80a4d-124">Specifies the name of the gateway.</span></span>
<span data-ttu-id="80a4d-125">Esse cmdlet cria uma chave para o gateway que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="80a4d-125">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

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

### <span data-ttu-id="80a4d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80a4d-126">-ResourceGroupName</span></span>
<span data-ttu-id="80a4d-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="80a4d-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="80a4d-128">Esse cmdlet cria uma chave para um gateway que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="80a4d-128">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a4d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a4d-129">-DefaultProfile</span></span>
<span data-ttu-id="80a4d-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80a4d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80a4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a4d-131">CommonParameters</span></span>
<span data-ttu-id="80a4d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a4d-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a4d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a4d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80a4d-134">INPUTS</span></span>

## <span data-ttu-id="80a4d-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80a4d-135">OUTPUTS</span></span>

### <span data-ttu-id="80a4d-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="80a4d-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="80a4d-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80a4d-137">NOTES</span></span>
* <span data-ttu-id="80a4d-138">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="80a4d-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="80a4d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80a4d-139">RELATED LINKS</span></span>

<span data-ttu-id="80a4d-140">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="80a4d-140">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>


