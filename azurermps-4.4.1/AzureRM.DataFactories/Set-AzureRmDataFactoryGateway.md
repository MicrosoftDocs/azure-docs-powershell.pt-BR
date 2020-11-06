---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 2cca641538be35f18173fd1e03b5f593c87649bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428248"
---
# <span data-ttu-id="e2ea5-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e2ea5-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="e2ea5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ea5-103">Define a descrição de um gateway na fábrica de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2ea5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2ea5-104">SYNTAX</span></span>

### <span data-ttu-id="e2ea5-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2ea5-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2ea5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e2ea5-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2ea5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2ea5-107">DESCRIPTION</span></span>
<span data-ttu-id="e2ea5-108">O cmdlet **set-AzureRmDataFactoryGateway** define a descrição do gateway especificado no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="e2ea5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2ea5-109">EXAMPLES</span></span>

### <span data-ttu-id="e2ea5-110">Exemplo 1: definir a descrição de um gateway</span><span class="sxs-lookup"><span data-stu-id="e2ea5-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="e2ea5-111">Esse comando define a descrição do gateway chamado ContosoGateway no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="e2ea5-112">O parâmetro Description especifica a nova descrição.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="e2ea5-113">OS</span><span class="sxs-lookup"><span data-stu-id="e2ea5-113">PARAMETERS</span></span>

### <span data-ttu-id="e2ea5-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="e2ea5-114">-DataFactory</span></span>
<span data-ttu-id="e2ea5-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="e2ea5-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e2ea5-116">Esse cmdlet define a descrição do gateway na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e2ea5-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e2ea5-117">-DataFactoryName</span></span>
<span data-ttu-id="e2ea5-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e2ea5-119">Esse cmdlet define a descrição do gateway na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e2ea5-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e2ea5-120">-Description</span></span>
<span data-ttu-id="e2ea5-121">Especifica uma descrição para o gateway.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-121">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ea5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2ea5-122">-Name</span></span>
<span data-ttu-id="e2ea5-123">Especifica o nome do gateway para o qual definir uma descrição.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-123">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="e2ea5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ea5-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2ea5-125">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e2ea5-126">Esse cmdlet define a descrição de um gateway que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-126">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e2ea5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ea5-127">-DefaultProfile</span></span>
<span data-ttu-id="e2ea5-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2ea5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ea5-129">CommonParameters</span></span>
<span data-ttu-id="e2ea5-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ea5-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2ea5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ea5-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2ea5-132">INPUTS</span></span>

## <span data-ttu-id="e2ea5-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2ea5-133">OUTPUTS</span></span>

### <span data-ttu-id="e2ea5-134">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e2ea5-134">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="e2ea5-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2ea5-135">NOTES</span></span>
* <span data-ttu-id="e2ea5-136">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="e2ea5-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e2ea5-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2ea5-137">RELATED LINKS</span></span>

[<span data-ttu-id="e2ea5-138">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e2ea5-138">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="e2ea5-139">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e2ea5-139">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="e2ea5-140">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e2ea5-140">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


