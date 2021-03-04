---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 678cc7e015321d90fee5a5340caeeeb861b30600
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887781"
---
# <span data-ttu-id="c5771-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="c5771-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="c5771-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5771-102">SYNOPSIS</span></span>
<span data-ttu-id="c5771-103">Criptografe a credencial no serviço vinculado com o tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="c5771-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="c5771-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c5771-104">SYNTAX</span></span>

### <span data-ttu-id="c5771-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c5771-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5771-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c5771-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5771-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c5771-107">DESCRIPTION</span></span>
<span data-ttu-id="c5771-108">O New-AzDataFactoryV2LinkedServiceEncryptedCredential de criptografia de cmdlet no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="c5771-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="c5771-109">Certifique-se de que os seguintes pré-requisitos sejam atendidos:</span><span class="sxs-lookup"><span data-stu-id="c5771-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="c5771-110">**A opção** de acesso remoto está habilitada no tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="c5771-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="c5771-111">O Powershell 7.0 ou superior é usado para executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5771-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="c5771-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5771-112">EXAMPLES</span></span>

### <span data-ttu-id="c5771-113">Exemplo 1: criptografar credenciais em um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="c5771-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="c5771-114">Este comando criptografa a credencial no arquivo C:\samples\WikiSample\TaxiDemo1.jscom o tempo de execução de integração chamado test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="c5771-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="c5771-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c5771-115">PARAMETERS</span></span>

### <span data-ttu-id="c5771-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c5771-116">-DataFactory</span></span>
<span data-ttu-id="c5771-117">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c5771-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5771-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c5771-118">-DataFactoryName</span></span>
<span data-ttu-id="c5771-119">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c5771-119">The data factory name.</span></span>

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

### <span data-ttu-id="c5771-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5771-120">-DefaultProfile</span></span>
<span data-ttu-id="c5771-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c5771-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5771-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c5771-122">-DefinitionFile</span></span>
<span data-ttu-id="c5771-123">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="c5771-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5771-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c5771-124">-Force</span></span>
<span data-ttu-id="c5771-125">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="c5771-125">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5771-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c5771-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="c5771-127">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5771-127">The integration runtime name.</span></span>

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

### <span data-ttu-id="c5771-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5771-128">-ResourceGroupName</span></span>
<span data-ttu-id="c5771-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5771-129">The resource group name.</span></span>

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

### <span data-ttu-id="c5771-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5771-130">-Confirm</span></span>
<span data-ttu-id="c5771-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5771-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5771-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5771-132">-WhatIf</span></span>
<span data-ttu-id="c5771-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5771-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c5771-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5771-134">CommonParameters</span></span>
<span data-ttu-id="c5771-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5771-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5771-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5771-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5771-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5771-137">INPUTS</span></span>

### <span data-ttu-id="c5771-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c5771-138">System.String</span></span>

### <span data-ttu-id="c5771-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c5771-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="c5771-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c5771-140">OUTPUTS</span></span>

### <span data-ttu-id="c5771-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c5771-141">System.String</span></span>

## <span data-ttu-id="c5771-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="c5771-142">NOTES</span></span>

## <span data-ttu-id="c5771-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5771-143">RELATED LINKS</span></span>
