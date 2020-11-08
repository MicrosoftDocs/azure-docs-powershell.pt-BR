---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112321"
---
# <span data-ttu-id="86d95-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="86d95-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="86d95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86d95-102">SYNOPSIS</span></span>
<span data-ttu-id="86d95-103">Cria a chave de autenticação para um gateway do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="86d95-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="86d95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86d95-104">SYNTAX</span></span>

### <span data-ttu-id="86d95-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="86d95-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86d95-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="86d95-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d95-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86d95-107">DESCRIPTION</span></span>
<span data-ttu-id="86d95-108">O cmdlet **New-AzDataFactoryGatewayAuthKey** cria a chave de autenticação de gateway para um gateway de fábrica de dados do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="86d95-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="86d95-109">Você registra o gateway com um serviço na nuvem usando essa chave.</span><span class="sxs-lookup"><span data-stu-id="86d95-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="86d95-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86d95-110">EXAMPLES</span></span>

### <span data-ttu-id="86d95-111">Exemplo 1: cria uma chave de autenticação de gateway para a key1</span><span class="sxs-lookup"><span data-stu-id="86d95-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="86d95-112">Esse comando cria uma chave de autenticação de gateway da key1 para o gateway de fábrica de dados denominado mygateway.</span><span class="sxs-lookup"><span data-stu-id="86d95-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="86d95-113">OS</span><span class="sxs-lookup"><span data-stu-id="86d95-113">PARAMETERS</span></span>

### <span data-ttu-id="86d95-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="86d95-114">-DataFactoryName</span></span>
<span data-ttu-id="86d95-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="86d95-115">The data factory name.</span></span>

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

### <span data-ttu-id="86d95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d95-116">-DefaultProfile</span></span>
<span data-ttu-id="86d95-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="86d95-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86d95-118">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="86d95-118">-GatewayName</span></span>
<span data-ttu-id="86d95-119">O nome do gateway de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="86d95-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="86d95-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86d95-120">-InputObject</span></span>
<span data-ttu-id="86d95-121">O objeto de fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="86d95-121">The data factory object</span></span>

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

### <span data-ttu-id="86d95-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="86d95-122">-KeyName</span></span>
<span data-ttu-id="86d95-123">O nome da chave de autenticação do gateway a ser regenerado, ' key1 ' ou ' Key2 '.</span><span class="sxs-lookup"><span data-stu-id="86d95-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d95-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d95-124">-ResourceGroupName</span></span>
<span data-ttu-id="86d95-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="86d95-125">The resource group name.</span></span>

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

### <span data-ttu-id="86d95-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="86d95-126">-Confirm</span></span>
<span data-ttu-id="86d95-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d95-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d95-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d95-128">-WhatIf</span></span>
<span data-ttu-id="86d95-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="86d95-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86d95-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="86d95-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d95-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d95-131">CommonParameters</span></span>
<span data-ttu-id="86d95-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d95-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d95-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d95-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d95-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86d95-134">INPUTS</span></span>

### <span data-ttu-id="86d95-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="86d95-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="86d95-136">System. String</span><span class="sxs-lookup"><span data-stu-id="86d95-136">System.String</span></span>

## <span data-ttu-id="86d95-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86d95-137">OUTPUTS</span></span>

### <span data-ttu-id="86d95-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="86d95-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="86d95-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86d95-139">NOTES</span></span>
* <span data-ttu-id="86d95-140">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="86d95-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="86d95-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86d95-141">RELATED LINKS</span></span>

<span data-ttu-id="86d95-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="86d95-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

