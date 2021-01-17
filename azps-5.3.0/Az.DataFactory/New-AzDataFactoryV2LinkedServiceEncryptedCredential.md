---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: a99f7fbb1383d685a53cc11f9dd81f6f306ed633
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429886"
---
# <span data-ttu-id="2dc17-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="2dc17-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="2dc17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dc17-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc17-103">Criptografar credencial no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="2dc17-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="2dc17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2dc17-104">SYNTAX</span></span>

### <span data-ttu-id="2dc17-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2dc17-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dc17-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2dc17-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dc17-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2dc17-107">DESCRIPTION</span></span>
<span data-ttu-id="2dc17-108">O cmdlet New-AzDataFactoryV2LinkedServiceEncryptedCredential criptografar credenciais no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="2dc17-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="2dc17-109">Certifique-se de que os seguintes pré-requisitos são atendidos:</span><span class="sxs-lookup"><span data-stu-id="2dc17-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="2dc17-110">A opção de **acesso remoto** está habilitada no tempo de execução de integração de hospedagem automática.</span><span class="sxs-lookup"><span data-stu-id="2dc17-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="2dc17-111">O PowerShell 7,0 ou posterior é usado para executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc17-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="2dc17-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2dc17-112">EXAMPLES</span></span>

### <span data-ttu-id="2dc17-113">Exemplo 1: criptografar credenciais em um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="2dc17-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="2dc17-114">Esse comando criptografa a credencial no arquivo C:\samples\WikiSample\TaxiDemo1.jscom o tempo de execução de integração chamado Test-selfhost-IV.</span><span class="sxs-lookup"><span data-stu-id="2dc17-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="2dc17-115">OS</span><span class="sxs-lookup"><span data-stu-id="2dc17-115">PARAMETERS</span></span>

### <span data-ttu-id="2dc17-116">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="2dc17-116">-DataFactory</span></span>
<span data-ttu-id="2dc17-117">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2dc17-117">The data factory object.</span></span>

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

### <span data-ttu-id="2dc17-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2dc17-118">-DataFactoryName</span></span>
<span data-ttu-id="2dc17-119">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="2dc17-119">The data factory name.</span></span>

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

### <span data-ttu-id="2dc17-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc17-120">-DefaultProfile</span></span>
<span data-ttu-id="2dc17-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2dc17-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dc17-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="2dc17-122">-DefinitionFile</span></span>
<span data-ttu-id="2dc17-123">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="2dc17-123">The JSON file path.</span></span>

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

### <span data-ttu-id="2dc17-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2dc17-124">-Force</span></span>
<span data-ttu-id="2dc17-125">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="2dc17-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2dc17-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="2dc17-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="2dc17-127">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="2dc17-127">The integration runtime name.</span></span>

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

### <span data-ttu-id="2dc17-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc17-128">-ResourceGroupName</span></span>
<span data-ttu-id="2dc17-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2dc17-129">The resource group name.</span></span>

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

### <span data-ttu-id="2dc17-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2dc17-130">-Confirm</span></span>
<span data-ttu-id="2dc17-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc17-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dc17-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dc17-132">-WhatIf</span></span>
<span data-ttu-id="2dc17-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc17-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2dc17-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc17-134">CommonParameters</span></span>
<span data-ttu-id="2dc17-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dc17-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc17-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dc17-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc17-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2dc17-137">INPUTS</span></span>

### <span data-ttu-id="2dc17-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2dc17-138">System.String</span></span>

### <span data-ttu-id="2dc17-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2dc17-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2dc17-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2dc17-140">OUTPUTS</span></span>

### <span data-ttu-id="2dc17-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2dc17-141">System.String</span></span>

## <span data-ttu-id="2dc17-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2dc17-142">NOTES</span></span>

## <span data-ttu-id="2dc17-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dc17-143">RELATED LINKS</span></span>
