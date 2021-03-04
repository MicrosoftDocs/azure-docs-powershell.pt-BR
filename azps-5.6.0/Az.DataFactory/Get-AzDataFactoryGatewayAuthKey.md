---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 7987f014b08250975a2a25323122a081d508b036
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888315"
---
# <span data-ttu-id="a9e8c-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="a9e8c-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="a9e8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e8c-103">Obtém a chave de auth do gateway para uma Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9e8c-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="a9e8c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a9e8c-104">SYNTAX</span></span>

### <span data-ttu-id="a9e8c-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a9e8c-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9e8c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a9e8c-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9e8c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a9e8c-107">DESCRIPTION</span></span>
<span data-ttu-id="a9e8c-108">O cmdlet **Get-AzDataFactoryGatewayAuthKey** obtém a chave de entrada de gateway para um gateway especificado da Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9e8c-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="a9e8c-109">Você registra o gateway com um serviço de nuvem usando essa chave1 ou chave2 dessa tecla de auth.</span><span class="sxs-lookup"><span data-stu-id="a9e8c-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="a9e8c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9e8c-110">EXAMPLES</span></span>

### <span data-ttu-id="a9e8c-111">Exemplo 1: obtém a tecla de auth de um gateway</span><span class="sxs-lookup"><span data-stu-id="a9e8c-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="a9e8c-112">Este comando obtém a chave de entrada de gateway para o gateway de fábrica de dados chamado MyGateway.</span><span class="sxs-lookup"><span data-stu-id="a9e8c-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="a9e8c-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a9e8c-113">PARAMETERS</span></span>

### <span data-ttu-id="a9e8c-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a9e8c-114">-DataFactoryName</span></span>
<span data-ttu-id="a9e8c-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="a9e8c-115">The data factory name.</span></span>

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

### <span data-ttu-id="a9e8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e8c-116">-DefaultProfile</span></span>
<span data-ttu-id="a9e8c-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a9e8c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9e8c-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="a9e8c-118">-GatewayName</span></span>
<span data-ttu-id="a9e8c-119">O nome do gateway de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="a9e8c-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="a9e8c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9e8c-120">-InputObject</span></span>
<span data-ttu-id="a9e8c-121">O objeto data factory</span><span class="sxs-lookup"><span data-stu-id="a9e8c-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e8c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e8c-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9e8c-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9e8c-123">The resource group name.</span></span>

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

### <span data-ttu-id="a9e8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e8c-124">CommonParameters</span></span>
<span data-ttu-id="a9e8c-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e8c-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e8c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e8c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9e8c-127">INPUTS</span></span>

### <span data-ttu-id="a9e8c-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9e8c-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a9e8c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a9e8c-129">System.String</span></span>

## <span data-ttu-id="a9e8c-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a9e8c-130">OUTPUTS</span></span>

### <span data-ttu-id="a9e8c-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="a9e8c-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="a9e8c-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="a9e8c-132">NOTES</span></span>
* <span data-ttu-id="a9e8c-133">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="a9e8c-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a9e8c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9e8c-134">RELATED LINKS</span></span>

<span data-ttu-id="a9e8c-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="a9e8c-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

