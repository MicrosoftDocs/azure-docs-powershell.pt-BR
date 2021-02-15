---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: b6647ab3b729ab76d3cc02687bcd8dc342e788b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115389"
---
# <span data-ttu-id="f2689-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="f2689-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="f2689-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2689-102">SYNOPSIS</span></span>
<span data-ttu-id="f2689-103">Adiciona um provedor de identidade confiável à conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2689-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f2689-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2689-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2689-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2689-105">DESCRIPTION</span></span>
<span data-ttu-id="f2689-106">O cmdlet **Add-AzDataLakeStoreTrustedIdProvider** adiciona um provedor de identidade confiável à conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2689-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f2689-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2689-107">EXAMPLES</span></span>

### <span data-ttu-id="f2689-108">Exemplo 1: Adicionar um provedor de identidade confiável</span><span class="sxs-lookup"><span data-stu-id="f2689-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="f2689-109">Adiciona o provedor "MeuProvider" à conta "ContosoADL" com o ponto de extremidade do provedor https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 " "</span><span class="sxs-lookup"><span data-stu-id="f2689-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="f2689-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2689-110">PARAMETERS</span></span>

### <span data-ttu-id="f2689-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="f2689-111">-Account</span></span>
<span data-ttu-id="f2689-112">O nome da conta do Data Lake Store para adicionar o provedor de identidade confiável especificado.</span><span class="sxs-lookup"><span data-stu-id="f2689-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="f2689-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2689-113">-DefaultProfile</span></span>
<span data-ttu-id="f2689-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f2689-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2689-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2689-115">-Name</span></span>
<span data-ttu-id="f2689-116">O nome do provedor de identidade confiável para adicionar</span><span class="sxs-lookup"><span data-stu-id="f2689-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="f2689-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2689-117">-ProviderEndpoint</span></span>
<span data-ttu-id="f2689-118">O ponto de extremidade do provedor confiável válido no formato: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="f2689-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="f2689-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2689-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2689-120">Nome do grupo de recursos no qual a conta para adicionar o provedor de identidade confiável é.</span><span class="sxs-lookup"><span data-stu-id="f2689-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="f2689-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f2689-121">-Confirm</span></span>
<span data-ttu-id="f2689-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2689-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2689-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2689-123">-WhatIf</span></span>
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

### <span data-ttu-id="f2689-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2689-124">CommonParameters</span></span>
<span data-ttu-id="f2689-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2689-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2689-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2689-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2689-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="f2689-127">INPUTS</span></span>

### <span data-ttu-id="f2689-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f2689-128">System.String</span></span>

## <span data-ttu-id="f2689-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="f2689-129">OUTPUTS</span></span>

### <span data-ttu-id="f2689-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="f2689-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="f2689-131">Notas</span><span class="sxs-lookup"><span data-stu-id="f2689-131">NOTES</span></span>

## <span data-ttu-id="f2689-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2689-132">RELATED LINKS</span></span>
