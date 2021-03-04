---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: e58df40aa227e1c8132902c467c2dbcb881c7b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888256"
---
# <span data-ttu-id="ae467-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="ae467-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="ae467-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae467-102">SYNOPSIS</span></span>
<span data-ttu-id="ae467-103">Cria uma chave de auth para um Gateway de Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae467-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="ae467-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae467-104">SYNTAX</span></span>

### <span data-ttu-id="ae467-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ae467-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae467-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ae467-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae467-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae467-107">DESCRIPTION</span></span>
<span data-ttu-id="ae467-108">O cmdlet **New-AzDataFactoryGatewayAuthKey** cria a chave de auth do gateway para um gateway especificado da Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae467-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="ae467-109">Você registra o gateway com um serviço de nuvem usando essa chave.</span><span class="sxs-lookup"><span data-stu-id="ae467-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="ae467-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae467-110">EXAMPLES</span></span>

### <span data-ttu-id="ae467-111">Exemplo 1: cria uma chave de auth de gateway para Key1</span><span class="sxs-lookup"><span data-stu-id="ae467-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="ae467-112">Este comando cria uma chave de auth de gateway de Key1 para o gateway de fábrica de dados chamado MyGateway.</span><span class="sxs-lookup"><span data-stu-id="ae467-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="ae467-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae467-113">PARAMETERS</span></span>

### <span data-ttu-id="ae467-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ae467-114">-DataFactoryName</span></span>
<span data-ttu-id="ae467-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ae467-115">The data factory name.</span></span>

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

### <span data-ttu-id="ae467-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae467-116">-DefaultProfile</span></span>
<span data-ttu-id="ae467-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ae467-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae467-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="ae467-118">-GatewayName</span></span>
<span data-ttu-id="ae467-119">O nome do gateway de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ae467-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="ae467-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae467-120">-InputObject</span></span>
<span data-ttu-id="ae467-121">O objeto data factory</span><span class="sxs-lookup"><span data-stu-id="ae467-121">The data factory object</span></span>

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

### <span data-ttu-id="ae467-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ae467-122">-KeyName</span></span>
<span data-ttu-id="ae467-123">O nome da chave de auth do gateway a ser regenerada, 'key1' ou 'key2'.</span><span class="sxs-lookup"><span data-stu-id="ae467-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="ae467-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae467-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae467-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae467-125">The resource group name.</span></span>

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

### <span data-ttu-id="ae467-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae467-126">-Confirm</span></span>
<span data-ttu-id="ae467-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae467-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae467-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae467-128">-WhatIf</span></span>
<span data-ttu-id="ae467-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae467-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae467-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae467-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae467-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae467-131">CommonParameters</span></span>
<span data-ttu-id="ae467-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae467-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae467-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae467-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae467-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae467-134">INPUTS</span></span>

### <span data-ttu-id="ae467-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ae467-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ae467-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ae467-136">System.String</span></span>

## <span data-ttu-id="ae467-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae467-137">OUTPUTS</span></span>

### <span data-ttu-id="ae467-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="ae467-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="ae467-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae467-139">NOTES</span></span>
* <span data-ttu-id="ae467-140">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="ae467-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ae467-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae467-141">RELATED LINKS</span></span>

<span data-ttu-id="ae467-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="ae467-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

