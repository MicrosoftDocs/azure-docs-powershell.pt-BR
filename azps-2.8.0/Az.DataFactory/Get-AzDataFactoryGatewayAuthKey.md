---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: ed1cbf5fb39ba89427260225ecad0b4b8b5b1461
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597083"
---
# <span data-ttu-id="46e60-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="46e60-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="46e60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46e60-102">SYNOPSIS</span></span>
<span data-ttu-id="46e60-103">Obtém a chave de autenticação de gateway para um Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="46e60-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="46e60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46e60-104">SYNTAX</span></span>

### <span data-ttu-id="46e60-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="46e60-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e60-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="46e60-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46e60-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46e60-107">DESCRIPTION</span></span>
<span data-ttu-id="46e60-108">O cmdlet **Get-AzDataFactoryGatewayAuthKey** Obtém a chave de autenticação de gateway para um gateway de fábrica de dados do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="46e60-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="46e60-109">Você registra o gateway com um serviço na nuvem usando esta key1 ou Key2 da chave de autenticação.</span><span class="sxs-lookup"><span data-stu-id="46e60-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="46e60-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46e60-110">EXAMPLES</span></span>

### <span data-ttu-id="46e60-111">Exemplo 1: Obtém a chave de autenticação de um gateway</span><span class="sxs-lookup"><span data-stu-id="46e60-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="46e60-112">Esse comando obtém a chave de autenticação de gateway do gateway de fábrica de dados denominado mygateway.</span><span class="sxs-lookup"><span data-stu-id="46e60-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="46e60-113">OS</span><span class="sxs-lookup"><span data-stu-id="46e60-113">PARAMETERS</span></span>

### <span data-ttu-id="46e60-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="46e60-114">-DataFactoryName</span></span>
<span data-ttu-id="46e60-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="46e60-115">The data factory name.</span></span>

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

### <span data-ttu-id="46e60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e60-116">-DefaultProfile</span></span>
<span data-ttu-id="46e60-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="46e60-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46e60-118">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="46e60-118">-GatewayName</span></span>
<span data-ttu-id="46e60-119">O nome do gateway de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="46e60-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="46e60-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46e60-120">-InputObject</span></span>
<span data-ttu-id="46e60-121">O objeto de fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="46e60-121">The data factory object</span></span>

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

### <span data-ttu-id="46e60-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e60-122">-ResourceGroupName</span></span>
<span data-ttu-id="46e60-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46e60-123">The resource group name.</span></span>

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

### <span data-ttu-id="46e60-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e60-124">CommonParameters</span></span>
<span data-ttu-id="46e60-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e60-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e60-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e60-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e60-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46e60-127">INPUTS</span></span>

### <span data-ttu-id="46e60-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="46e60-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="46e60-129">System. String</span><span class="sxs-lookup"><span data-stu-id="46e60-129">System.String</span></span>

## <span data-ttu-id="46e60-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46e60-130">OUTPUTS</span></span>

### <span data-ttu-id="46e60-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="46e60-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="46e60-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46e60-132">NOTES</span></span>
* <span data-ttu-id="46e60-133">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="46e60-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="46e60-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46e60-134">RELATED LINKS</span></span>

<span data-ttu-id="46e60-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="46e60-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

