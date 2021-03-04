---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 11d87742e34ae387f765551f93add5a1c300421a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887784"
---
# <span data-ttu-id="65496-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="65496-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="65496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65496-102">SYNOPSIS</span></span>
<span data-ttu-id="65496-103">Regenerar a chave de tempo de execução de integração auto-hospedada.</span><span class="sxs-lookup"><span data-stu-id="65496-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="65496-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65496-104">SYNTAX</span></span>

### <span data-ttu-id="65496-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="65496-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65496-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65496-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65496-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="65496-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65496-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65496-108">DESCRIPTION</span></span>
<span data-ttu-id="65496-109">O cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenera a chave de tempo de execução de integração com o nome da chave especificado pelo parâmetro 'KeyName'.</span><span class="sxs-lookup"><span data-stu-id="65496-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="65496-110">A chave anterior será inválida.</span><span class="sxs-lookup"><span data-stu-id="65496-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="65496-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65496-111">EXAMPLES</span></span>

### <span data-ttu-id="65496-112">Exemplo 1: Gerar uma nova chave para um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="65496-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="65496-113">O cmdlet regenera a chave 'authKey2' para o tempo de execução de integração chamado 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="65496-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="65496-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65496-114">PARAMETERS</span></span>

### <span data-ttu-id="65496-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="65496-115">-DataFactoryName</span></span>
<span data-ttu-id="65496-116">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="65496-116">The data factory name.</span></span>

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

### <span data-ttu-id="65496-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65496-117">-DefaultProfile</span></span>
<span data-ttu-id="65496-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="65496-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65496-119">-Force</span><span class="sxs-lookup"><span data-stu-id="65496-119">-Force</span></span>
<span data-ttu-id="65496-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="65496-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="65496-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65496-121">-InputObject</span></span>
<span data-ttu-id="65496-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="65496-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="65496-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="65496-123">-KeyName</span></span>
<span data-ttu-id="65496-124">O nome da chave de autenticação do tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="65496-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="65496-125">-Name</span><span class="sxs-lookup"><span data-stu-id="65496-125">-Name</span></span>
<span data-ttu-id="65496-126">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="65496-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="65496-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65496-127">-ResourceGroupName</span></span>
<span data-ttu-id="65496-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65496-128">The resource group name.</span></span>

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

### <span data-ttu-id="65496-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65496-129">-ResourceId</span></span>
<span data-ttu-id="65496-130">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="65496-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="65496-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65496-131">-Confirm</span></span>
<span data-ttu-id="65496-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65496-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65496-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65496-133">-WhatIf</span></span>
<span data-ttu-id="65496-134">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65496-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="65496-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65496-135">CommonParameters</span></span>
<span data-ttu-id="65496-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65496-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65496-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65496-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65496-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65496-138">INPUTS</span></span>

### <span data-ttu-id="65496-139">System.String</span><span class="sxs-lookup"><span data-stu-id="65496-139">System.String</span></span>

### <span data-ttu-id="65496-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="65496-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="65496-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65496-141">OUTPUTS</span></span>

### <span data-ttu-id="65496-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="65496-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="65496-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="65496-143">NOTES</span></span>

## <span data-ttu-id="65496-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65496-144">RELATED LINKS</span></span>

[<span data-ttu-id="65496-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="65496-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
