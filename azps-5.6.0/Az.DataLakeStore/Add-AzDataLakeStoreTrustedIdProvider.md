---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 31ac134dc580fc23876a2fd4f9b75e60b23748e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890863"
---
# <span data-ttu-id="5f26e-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="5f26e-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="5f26e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f26e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f26e-103">Adiciona um provedor de identidade confiável à conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5f26e-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="5f26e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5f26e-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f26e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5f26e-105">DESCRIPTION</span></span>
<span data-ttu-id="5f26e-106">O cmdlet **Add-AzDataLakeStoreTrustedIdProvider** adiciona um provedor de identidade confiável à conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5f26e-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="5f26e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f26e-107">EXAMPLES</span></span>

### <span data-ttu-id="5f26e-108">Exemplo 1: Adicionar um provedor de identidade confiável</span><span class="sxs-lookup"><span data-stu-id="5f26e-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="5f26e-109">Adiciona o provedor "MyProvider" à conta "ContosoADL" com o ponto de extremidade do provedor https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 " "</span><span class="sxs-lookup"><span data-stu-id="5f26e-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="5f26e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5f26e-110">PARAMETERS</span></span>

### <span data-ttu-id="5f26e-111">-Account</span><span class="sxs-lookup"><span data-stu-id="5f26e-111">-Account</span></span>
<span data-ttu-id="5f26e-112">O nome da conta do Data Lake Store para adicionar o provedor de identidade confiável especificado.</span><span class="sxs-lookup"><span data-stu-id="5f26e-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f26e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f26e-113">-DefaultProfile</span></span>
<span data-ttu-id="5f26e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5f26e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f26e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5f26e-115">-Name</span></span>
<span data-ttu-id="5f26e-116">O nome do provedor de identidade confiável a ser acrescentado</span><span class="sxs-lookup"><span data-stu-id="5f26e-116">The name of the trusted identity provider to add</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f26e-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f26e-117">-ProviderEndpoint</span></span>
<span data-ttu-id="5f26e-118">O ponto de extremidade de provedor confiável válido no formato: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="5f26e-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="5f26e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f26e-119">-ResourceGroupName</span></span>
<span data-ttu-id="5f26e-120">Nome do grupo de recursos no qual a conta para adicionar o provedor de identidade confiável é.</span><span class="sxs-lookup"><span data-stu-id="5f26e-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f26e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f26e-121">-Confirm</span></span>
<span data-ttu-id="5f26e-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f26e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f26e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f26e-123">-WhatIf</span></span>
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

### <span data-ttu-id="5f26e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f26e-124">CommonParameters</span></span>
<span data-ttu-id="5f26e-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f26e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f26e-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f26e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f26e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f26e-127">INPUTS</span></span>

### <span data-ttu-id="5f26e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5f26e-128">System.String</span></span>

## <span data-ttu-id="5f26e-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5f26e-129">OUTPUTS</span></span>

### <span data-ttu-id="5f26e-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="5f26e-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="5f26e-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="5f26e-131">NOTES</span></span>

## <span data-ttu-id="5f26e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f26e-132">RELATED LINKS</span></span>
