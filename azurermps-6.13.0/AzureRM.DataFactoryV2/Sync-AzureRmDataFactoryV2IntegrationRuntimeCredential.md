---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/sync-azurermdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 05b9c5bce3158413f562c38eb116523609696523
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430320"
---
# <span data-ttu-id="0c370-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="0c370-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="0c370-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c370-102">SYNOPSIS</span></span>
<span data-ttu-id="0c370-103">Sincroniza as credenciais entre nós do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="0c370-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c370-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c370-104">SYNTAX</span></span>

### <span data-ttu-id="0c370-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0c370-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c370-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c370-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c370-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0c370-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c370-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c370-108">DESCRIPTION</span></span>
<span data-ttu-id="0c370-109">O cmdlet **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** sincroniza as credenciais locais entre nós do tempo de execução de integração, o que obriga as credenciais a serem idênticas em todos os nós.</span><span class="sxs-lookup"><span data-stu-id="0c370-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="0c370-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c370-110">EXAMPLES</span></span>

### <span data-ttu-id="0c370-111">Exemplo 1: sincronizar uma credencial de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="0c370-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="0c370-112">O cmdlet sincroniza credenciais entre nós do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="0c370-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="0c370-113">OS</span><span class="sxs-lookup"><span data-stu-id="0c370-113">PARAMETERS</span></span>

### <span data-ttu-id="0c370-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0c370-114">-DataFactoryName</span></span>
<span data-ttu-id="0c370-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="0c370-115">The data factory name.</span></span>

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

### <span data-ttu-id="0c370-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c370-116">-DefaultProfile</span></span>
<span data-ttu-id="0c370-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c370-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c370-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0c370-118">-Force</span></span>
<span data-ttu-id="0c370-119">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="0c370-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0c370-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c370-120">-InputObject</span></span>
<span data-ttu-id="0c370-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="0c370-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="0c370-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="0c370-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="0c370-123">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="0c370-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c370-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c370-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c370-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c370-125">The resource group name.</span></span>

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

### <span data-ttu-id="0c370-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c370-126">-ResourceId</span></span>
<span data-ttu-id="0c370-127">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c370-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0c370-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0c370-128">-Confirm</span></span>
<span data-ttu-id="0c370-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c370-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c370-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c370-130">-WhatIf</span></span>
<span data-ttu-id="0c370-131">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c370-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0c370-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c370-132">CommonParameters</span></span>
<span data-ttu-id="0c370-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c370-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c370-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c370-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c370-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c370-135">INPUTS</span></span>

### <span data-ttu-id="0c370-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0c370-136">System.String</span></span>

### <span data-ttu-id="0c370-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0c370-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="0c370-138">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c370-138">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0c370-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c370-139">OUTPUTS</span></span>

### <span data-ttu-id="0c370-140">System. void</span><span class="sxs-lookup"><span data-stu-id="0c370-140">System.Void</span></span>

## <span data-ttu-id="0c370-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c370-141">NOTES</span></span>

## <span data-ttu-id="0c370-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c370-142">RELATED LINKS</span></span>
