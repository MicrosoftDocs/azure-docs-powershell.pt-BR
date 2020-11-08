---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: b6647ab3b729ab76d3cc02687bcd8dc342e788b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111136"
---
# <span data-ttu-id="19d31-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="19d31-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="19d31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19d31-102">SYNOPSIS</span></span>
<span data-ttu-id="19d31-103">Adiciona um provedor de identidade confiável à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="19d31-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="19d31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19d31-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19d31-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19d31-105">DESCRIPTION</span></span>
<span data-ttu-id="19d31-106">O cmdlet **Add-AzDataLakeStoreTrustedIdProvider** adiciona um provedor de identidade confiável à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="19d31-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="19d31-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19d31-107">EXAMPLES</span></span>

### <span data-ttu-id="19d31-108">Exemplo 1: adicionar um provedor de identidade confiável</span><span class="sxs-lookup"><span data-stu-id="19d31-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="19d31-109">Adiciona o provedor "MyProvider" à conta "ContosoADL" com o ponto de extremidade do provedor " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="19d31-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="19d31-110">OS</span><span class="sxs-lookup"><span data-stu-id="19d31-110">PARAMETERS</span></span>

### <span data-ttu-id="19d31-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="19d31-111">-Account</span></span>
<span data-ttu-id="19d31-112">O nome da conta do data Lake Store para a qual o provedor de identidade confiável especificado será adicionado.</span><span class="sxs-lookup"><span data-stu-id="19d31-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="19d31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d31-113">-DefaultProfile</span></span>
<span data-ttu-id="19d31-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="19d31-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19d31-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="19d31-115">-Name</span></span>
<span data-ttu-id="19d31-116">O nome do provedor de identidade confiável a ser adicionado</span><span class="sxs-lookup"><span data-stu-id="19d31-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="19d31-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d31-117">-ProviderEndpoint</span></span>
<span data-ttu-id="19d31-118">O ponto de extremidade do provedor confiável válido no formato: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="19d31-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="19d31-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19d31-119">-ResourceGroupName</span></span>
<span data-ttu-id="19d31-120">Nome do grupo de recursos sob o qual a conta para a qual o provedor de identidade confiável será adicionado.</span><span class="sxs-lookup"><span data-stu-id="19d31-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="19d31-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19d31-121">-Confirm</span></span>
<span data-ttu-id="19d31-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19d31-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19d31-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19d31-123">-WhatIf</span></span>
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

### <span data-ttu-id="19d31-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d31-124">CommonParameters</span></span>
<span data-ttu-id="19d31-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19d31-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d31-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d31-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d31-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19d31-127">INPUTS</span></span>

### <span data-ttu-id="19d31-128">System. String</span><span class="sxs-lookup"><span data-stu-id="19d31-128">System.String</span></span>

## <span data-ttu-id="19d31-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19d31-129">OUTPUTS</span></span>

### <span data-ttu-id="19d31-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="19d31-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="19d31-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19d31-131">NOTES</span></span>

## <span data-ttu-id="19d31-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19d31-132">RELATED LINKS</span></span>
