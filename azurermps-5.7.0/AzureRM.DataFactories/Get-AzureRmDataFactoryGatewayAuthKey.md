---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 9e677417ed1d592da04d8023a7cc58826662fada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602739"
---
# <span data-ttu-id="ff9b7-101">Get-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="ff9b7-101">Get-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="ff9b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9b7-103">Obtém a chave de autenticação de gateway para um Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="ff9b7-103">Gets gateway auth key for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff9b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff9b7-104">SYNTAX</span></span>

### <span data-ttu-id="ff9b7-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ff9b7-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff9b7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ff9b7-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff9b7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff9b7-107">DESCRIPTION</span></span>
<span data-ttu-id="ff9b7-108">O cmdlet **Get-AzureRmDataFactoryGatewayAuthKey** Obtém a chave de autenticação de gateway para um gateway de fábrica de dados do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="ff9b7-108">The **Get-AzureRmDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="ff9b7-109">Você registra o gateway com um serviço na nuvem usando esta key1 ou Key2 da chave de autenticação.</span><span class="sxs-lookup"><span data-stu-id="ff9b7-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="ff9b7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff9b7-110">EXAMPLES</span></span>

### <span data-ttu-id="ff9b7-111">Exemplo 1: Obtém a chave de autenticação de um gateway</span><span class="sxs-lookup"><span data-stu-id="ff9b7-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="ff9b7-112">Esse comando obtém a chave de autenticação de gateway do gateway de fábrica de dados denominado mygateway.</span><span class="sxs-lookup"><span data-stu-id="ff9b7-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="ff9b7-113">OS</span><span class="sxs-lookup"><span data-stu-id="ff9b7-113">PARAMETERS</span></span>

### <span data-ttu-id="ff9b7-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ff9b7-114">-DataFactoryName</span></span>
<span data-ttu-id="ff9b7-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="ff9b7-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9b7-116">-DefaultProfile</span></span>
<span data-ttu-id="ff9b7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ff9b7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff9b7-118">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="ff9b7-118">-GatewayName</span></span>
<span data-ttu-id="ff9b7-119">O nome do gateway de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ff9b7-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="ff9b7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff9b7-120">-InputObject</span></span>
<span data-ttu-id="ff9b7-121">O objeto de fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="ff9b7-121">The data factory object</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9b7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff9b7-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff9b7-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff9b7-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9b7-124">CommonParameters</span></span>
<span data-ttu-id="ff9b7-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff9b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9b7-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff9b7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9b7-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff9b7-127">INPUTS</span></span>

### <span data-ttu-id="ff9b7-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff9b7-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="ff9b7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ff9b7-129">System.String</span></span>

## <span data-ttu-id="ff9b7-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff9b7-130">OUTPUTS</span></span>

### <span data-ttu-id="ff9b7-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="ff9b7-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="ff9b7-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff9b7-132">NOTES</span></span>
* <span data-ttu-id="ff9b7-133">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="ff9b7-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ff9b7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff9b7-134">RELATED LINKS</span></span>

<span data-ttu-id="ff9b7-135">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="ff9b7-135">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

