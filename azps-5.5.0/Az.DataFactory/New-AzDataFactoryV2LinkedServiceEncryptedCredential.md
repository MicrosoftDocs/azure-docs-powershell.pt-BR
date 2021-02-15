---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: a99f7fbb1383d685a53cc11f9dd81f6f306ed633
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118814"
---
# <span data-ttu-id="6eaed-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="6eaed-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="6eaed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6eaed-102">SYNOPSIS</span></span>
<span data-ttu-id="6eaed-103">Criptografe credenciais no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="6eaed-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="6eaed-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6eaed-104">SYNTAX</span></span>

### <span data-ttu-id="6eaed-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="6eaed-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eaed-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6eaed-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eaed-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6eaed-107">DESCRIPTION</span></span>
<span data-ttu-id="6eaed-108">O New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet criptografa credenciais no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="6eaed-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="6eaed-109">Certifique-se de que os seguintes pré-requisitos sejam atendidos:</span><span class="sxs-lookup"><span data-stu-id="6eaed-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="6eaed-110">**A opção** de acesso remoto está habilitada no tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="6eaed-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="6eaed-111">O Powershell 7.0 ou superior é usado para executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eaed-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="6eaed-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6eaed-112">EXAMPLES</span></span>

### <span data-ttu-id="6eaed-113">Exemplo 1: Criptografar credenciais em um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="6eaed-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="6eaed-114">Esse comando criptografa a credencial no arquivo C:\samples\WikiSample\TaxiDemo1.jscom o tempo de execução de integração chamado test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="6eaed-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="6eaed-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6eaed-115">PARAMETERS</span></span>

### <span data-ttu-id="6eaed-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6eaed-116">-DataFactory</span></span>
<span data-ttu-id="6eaed-117">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="6eaed-117">The data factory object.</span></span>

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

### <span data-ttu-id="6eaed-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6eaed-118">-DataFactoryName</span></span>
<span data-ttu-id="6eaed-119">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="6eaed-119">The data factory name.</span></span>

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

### <span data-ttu-id="6eaed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eaed-120">-DefaultProfile</span></span>
<span data-ttu-id="6eaed-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6eaed-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eaed-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="6eaed-122">-DefinitionFile</span></span>
<span data-ttu-id="6eaed-123">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="6eaed-123">The JSON file path.</span></span>

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

### <span data-ttu-id="6eaed-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="6eaed-124">-Force</span></span>
<span data-ttu-id="6eaed-125">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="6eaed-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6eaed-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6eaed-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6eaed-127">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="6eaed-127">The integration runtime name.</span></span>

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

### <span data-ttu-id="6eaed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eaed-128">-ResourceGroupName</span></span>
<span data-ttu-id="6eaed-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6eaed-129">The resource group name.</span></span>

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

### <span data-ttu-id="6eaed-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6eaed-130">-Confirm</span></span>
<span data-ttu-id="6eaed-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eaed-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eaed-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eaed-132">-WhatIf</span></span>
<span data-ttu-id="6eaed-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eaed-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6eaed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eaed-134">CommonParameters</span></span>
<span data-ttu-id="6eaed-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eaed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eaed-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eaed-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eaed-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="6eaed-137">INPUTS</span></span>

### <span data-ttu-id="6eaed-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6eaed-138">System.String</span></span>

### <span data-ttu-id="6eaed-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6eaed-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6eaed-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="6eaed-140">OUTPUTS</span></span>

### <span data-ttu-id="6eaed-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6eaed-141">System.String</span></span>

## <span data-ttu-id="6eaed-142">Notas</span><span class="sxs-lookup"><span data-stu-id="6eaed-142">NOTES</span></span>

## <span data-ttu-id="6eaed-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6eaed-143">RELATED LINKS</span></span>
