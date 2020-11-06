---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 765bd2c75a377204ab4566f47d0498deaf127953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426390"
---
# <span data-ttu-id="13cb7-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="13cb7-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="13cb7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="13cb7-103">Criptografar credencial no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="13cb7-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13cb7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13cb7-104">SYNTAX</span></span>

### <span data-ttu-id="13cb7-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="13cb7-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13cb7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="13cb7-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13cb7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13cb7-107">DESCRIPTION</span></span>
<span data-ttu-id="13cb7-108">O cmdlet New-AzureRmDataFactoryV2LinkedServiceEncryptCredential criptografar credenciais no serviço vinculado com tempo de execução de integração especificado.</span><span class="sxs-lookup"><span data-stu-id="13cb7-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="13cb7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13cb7-109">EXAMPLES</span></span>

### <span data-ttu-id="13cb7-110">Exemplo 1: criptografar o creadentials em um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="13cb7-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="13cb7-111">Esse comando criptografa a credencial no arquivo D:\sql.jscom o tempo de execução de integração chamado myIR.</span><span class="sxs-lookup"><span data-stu-id="13cb7-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="13cb7-112">OS</span><span class="sxs-lookup"><span data-stu-id="13cb7-112">PARAMETERS</span></span>

### <span data-ttu-id="13cb7-113">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="13cb7-113">-DataFactory</span></span>
<span data-ttu-id="13cb7-114">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="13cb7-114">The data factory object.</span></span>

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

### <span data-ttu-id="13cb7-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="13cb7-115">-DataFactoryName</span></span>
<span data-ttu-id="13cb7-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="13cb7-116">The data factory name.</span></span>

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

### <span data-ttu-id="13cb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13cb7-117">-DefaultProfile</span></span>
<span data-ttu-id="13cb7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13cb7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13cb7-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="13cb7-119">-DefinitionFile</span></span>
<span data-ttu-id="13cb7-120">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="13cb7-120">The JSON file path.</span></span>

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

### <span data-ttu-id="13cb7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="13cb7-121">-Force</span></span>
<span data-ttu-id="13cb7-122">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="13cb7-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="13cb7-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="13cb7-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="13cb7-124">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="13cb7-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="13cb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13cb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="13cb7-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13cb7-126">The resource group name.</span></span>

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

### <span data-ttu-id="13cb7-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="13cb7-127">-Confirm</span></span>
<span data-ttu-id="13cb7-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13cb7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13cb7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13cb7-129">-WhatIf</span></span>
<span data-ttu-id="13cb7-130">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13cb7-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="13cb7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13cb7-131">CommonParameters</span></span>
<span data-ttu-id="13cb7-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13cb7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13cb7-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13cb7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13cb7-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13cb7-134">INPUTS</span></span>

### <span data-ttu-id="13cb7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="13cb7-135">System.String</span></span>

### <span data-ttu-id="13cb7-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="13cb7-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="13cb7-137">Parâmetros: datafactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13cb7-137">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="13cb7-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13cb7-138">OUTPUTS</span></span>

### <span data-ttu-id="13cb7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="13cb7-139">System.String</span></span>

## <span data-ttu-id="13cb7-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13cb7-140">NOTES</span></span>

## <span data-ttu-id="13cb7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13cb7-141">RELATED LINKS</span></span>
