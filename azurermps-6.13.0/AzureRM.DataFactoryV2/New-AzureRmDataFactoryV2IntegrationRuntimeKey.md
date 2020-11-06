---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: a3bccd635c5bb2a91cb0b8ea9bc09f93070d447d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428507"
---
# <span data-ttu-id="0a119-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0a119-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="0a119-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a119-102">SYNOPSIS</span></span>
<span data-ttu-id="0a119-103">Regenerar a chave de tempo de execução de integração de hospedagem automática.</span><span class="sxs-lookup"><span data-stu-id="0a119-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a119-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a119-104">SYNTAX</span></span>

### <span data-ttu-id="0a119-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0a119-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a119-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0a119-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a119-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0a119-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a119-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a119-108">DESCRIPTION</span></span>
<span data-ttu-id="0a119-109">O cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenera a chave de tempo de execução de integração com o nome de chave especificado pelo parâmetro ' KeyName '.</span><span class="sxs-lookup"><span data-stu-id="0a119-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="0a119-110">A chave anterior será inválida.</span><span class="sxs-lookup"><span data-stu-id="0a119-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="0a119-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a119-111">EXAMPLES</span></span>

### <span data-ttu-id="0a119-112">Exemplo 1: gerar uma nova chave para um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="0a119-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="0a119-113">O cmdlet regenera a chave "authKey2" para o tempo de execução de integração chamado "Test-selfhost-IV".</span><span class="sxs-lookup"><span data-stu-id="0a119-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="0a119-114">OS</span><span class="sxs-lookup"><span data-stu-id="0a119-114">PARAMETERS</span></span>

### <span data-ttu-id="0a119-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0a119-115">-DataFactoryName</span></span>
<span data-ttu-id="0a119-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="0a119-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a119-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a119-117">-DefaultProfile</span></span>
<span data-ttu-id="0a119-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a119-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a119-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0a119-119">-Force</span></span>
<span data-ttu-id="0a119-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="0a119-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0a119-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a119-121">-InputObject</span></span>
<span data-ttu-id="0a119-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="0a119-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a119-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0a119-123">-KeyName</span></span>
<span data-ttu-id="0a119-124">O nome da chave de autenticação do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="0a119-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a119-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a119-125">-Name</span></span>
<span data-ttu-id="0a119-126">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="0a119-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a119-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a119-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a119-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a119-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a119-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a119-129">-ResourceId</span></span>
<span data-ttu-id="0a119-130">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="0a119-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a119-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0a119-131">-Confirm</span></span>
<span data-ttu-id="0a119-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a119-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a119-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a119-133">-WhatIf</span></span>
<span data-ttu-id="0a119-134">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a119-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0a119-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a119-135">CommonParameters</span></span>
<span data-ttu-id="0a119-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a119-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a119-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a119-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a119-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a119-138">INPUTS</span></span>

### <span data-ttu-id="0a119-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0a119-139">System.String</span></span>

### <span data-ttu-id="0a119-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0a119-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="0a119-141">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0a119-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0a119-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a119-142">OUTPUTS</span></span>

### <span data-ttu-id="0a119-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="0a119-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="0a119-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a119-144">NOTES</span></span>

## <span data-ttu-id="0a119-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a119-145">RELATED LINKS</span></span>

[<span data-ttu-id="0a119-146">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0a119-146">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
