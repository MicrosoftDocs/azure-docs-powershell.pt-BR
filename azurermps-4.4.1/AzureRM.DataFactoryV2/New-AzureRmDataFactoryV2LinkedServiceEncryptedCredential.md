---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 9960a34d19c4016461ddfc53a37f83d3e73e7526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610014"
---
# <span data-ttu-id="f1b85-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="f1b85-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="f1b85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1b85-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b85-103">Criptografar credencial no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="f1b85-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1b85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1b85-104">SYNTAX</span></span>

### <span data-ttu-id="f1b85-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1b85-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f1b85-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f1b85-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f1b85-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1b85-107">DESCRIPTION</span></span>
<span data-ttu-id="f1b85-108">O cmdlet New-AzureRmDataFactoryV2LinkedServiceEncryptCredential criptografar credenciais no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="f1b85-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="f1b85-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1b85-109">EXAMPLES</span></span>

### <span data-ttu-id="f1b85-110">Exemplo 1: criptografar o creadentials em um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="f1b85-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="f1b85-111">Esse comando criptografa a credencial no arquivo D:\sql.jscom o tempo de execução de integração chamado myIR.</span><span class="sxs-lookup"><span data-stu-id="f1b85-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="f1b85-112">OS</span><span class="sxs-lookup"><span data-stu-id="f1b85-112">PARAMETERS</span></span>

### <span data-ttu-id="f1b85-113">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="f1b85-113">-DataFactory</span></span>
<span data-ttu-id="f1b85-114">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f1b85-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b85-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f1b85-115">-DataFactoryName</span></span>
<span data-ttu-id="f1b85-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="f1b85-116">The data factory name.</span></span>

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

### <span data-ttu-id="f1b85-117">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="f1b85-117">-DefinitionFile</span></span>
<span data-ttu-id="f1b85-118">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="f1b85-118">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b85-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f1b85-119">-Force</span></span>
<span data-ttu-id="f1b85-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f1b85-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b85-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f1b85-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f1b85-122">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="f1b85-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="f1b85-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b85-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1b85-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1b85-124">The resource group name.</span></span>

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

### <span data-ttu-id="f1b85-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1b85-125">-Confirm</span></span>
<span data-ttu-id="f1b85-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1b85-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b85-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1b85-127">-WhatIf</span></span>
<span data-ttu-id="f1b85-128">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1b85-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="f1b85-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1b85-129">INPUTS</span></span>

### <span data-ttu-id="f1b85-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f1b85-130">System.String</span></span>
<span data-ttu-id="f1b85-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f1b85-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="f1b85-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1b85-132">OUTPUTS</span></span>

### <span data-ttu-id="f1b85-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f1b85-133">System.String</span></span>


## <span data-ttu-id="f1b85-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1b85-134">NOTES</span></span>

## <span data-ttu-id="f1b85-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1b85-135">RELATED LINKS</span></span>

