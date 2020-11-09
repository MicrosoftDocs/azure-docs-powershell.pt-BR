---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 0ff9ef1337a1f2a5f0503c59dc4e6240d3c959b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281016"
---
# <span data-ttu-id="e779c-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="e779c-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="e779c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e779c-102">SYNOPSIS</span></span>
<span data-ttu-id="e779c-103">Criptografar credencial no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="e779c-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="e779c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e779c-104">SYNTAX</span></span>

### <span data-ttu-id="e779c-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e779c-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e779c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e779c-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e779c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e779c-107">DESCRIPTION</span></span>
<span data-ttu-id="e779c-108">O cmdlet New-AzDataFactoryV2LinkedServiceEncryptedCredential criptografar credenciais no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="e779c-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="e779c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e779c-109">EXAMPLES</span></span>

### <span data-ttu-id="e779c-110">Exemplo 1: criptografar credenciais em um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="e779c-110">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="e779c-111">Esse comando criptografa a credencial no arquivo C:\samples\WikiSample\TaxiDemo1.jscom o tempo de execução de integração chamado Test-selfhost-IV.</span><span class="sxs-lookup"><span data-stu-id="e779c-111">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="e779c-112">OS</span><span class="sxs-lookup"><span data-stu-id="e779c-112">PARAMETERS</span></span>

### <span data-ttu-id="e779c-113">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="e779c-113">-DataFactory</span></span>
<span data-ttu-id="e779c-114">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e779c-114">The data factory object.</span></span>

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

### <span data-ttu-id="e779c-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e779c-115">-DataFactoryName</span></span>
<span data-ttu-id="e779c-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e779c-116">The data factory name.</span></span>

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

### <span data-ttu-id="e779c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e779c-117">-DefaultProfile</span></span>
<span data-ttu-id="e779c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e779c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e779c-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e779c-119">-DefinitionFile</span></span>
<span data-ttu-id="e779c-120">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="e779c-120">The JSON file path.</span></span>

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

### <span data-ttu-id="e779c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e779c-121">-Force</span></span>
<span data-ttu-id="e779c-122">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="e779c-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e779c-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e779c-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="e779c-124">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="e779c-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="e779c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e779c-125">-ResourceGroupName</span></span>
<span data-ttu-id="e779c-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e779c-126">The resource group name.</span></span>

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

### <span data-ttu-id="e779c-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e779c-127">-Confirm</span></span>
<span data-ttu-id="e779c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e779c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e779c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e779c-129">-WhatIf</span></span>
<span data-ttu-id="e779c-130">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e779c-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e779c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e779c-131">CommonParameters</span></span>
<span data-ttu-id="e779c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e779c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e779c-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e779c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e779c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e779c-134">INPUTS</span></span>

### <span data-ttu-id="e779c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e779c-135">System.String</span></span>

### <span data-ttu-id="e779c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e779c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e779c-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e779c-137">OUTPUTS</span></span>

### <span data-ttu-id="e779c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e779c-138">System.String</span></span>

## <span data-ttu-id="e779c-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e779c-139">NOTES</span></span>

## <span data-ttu-id="e779c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e779c-140">RELATED LINKS</span></span>
