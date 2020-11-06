---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: f71fefdce069f1786125f8c65ba94d66fb67fa56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427945"
---
# <span data-ttu-id="e91fc-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="e91fc-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="e91fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e91fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e91fc-103">Adiciona um provedor de identidade confiável à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e91fc-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e91fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e91fc-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e91fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e91fc-105">DESCRIPTION</span></span>
<span data-ttu-id="e91fc-106">O cmdlet **Add-AzureRmDataLakeStoreTrustedIdProvider** adiciona um provedor de identidade confiável à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e91fc-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="e91fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e91fc-107">EXAMPLES</span></span>

### <span data-ttu-id="e91fc-108">Exemplo 1: adicionar um provedor de identidade confiável</span><span class="sxs-lookup"><span data-stu-id="e91fc-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="e91fc-109">Adiciona o provedor "MyProvider" à conta "ContosoADL" com o ponto de extremidade do provedor " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="e91fc-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="e91fc-110">OS</span><span class="sxs-lookup"><span data-stu-id="e91fc-110">PARAMETERS</span></span>

### <span data-ttu-id="e91fc-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="e91fc-111">-Account</span></span>
<span data-ttu-id="e91fc-112">O nome da conta do data Lake Store para a qual o provedor de identidade confiável especificado será adicionado.</span><span class="sxs-lookup"><span data-stu-id="e91fc-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="e91fc-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e91fc-113">-Name</span></span>
<span data-ttu-id="e91fc-114">O nome do provedor de identidade confiável a ser adicionado</span><span class="sxs-lookup"><span data-stu-id="e91fc-114">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="e91fc-115">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="e91fc-115">-ProviderEndpoint</span></span>
<span data-ttu-id="e91fc-116">O ponto de extremidade do provedor confiável válido no formato: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="e91fc-116">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="e91fc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e91fc-117">-ResourceGroupName</span></span>
<span data-ttu-id="e91fc-118">Nome do grupo de recursos sob o qual a conta para a qual o provedor de identidade confiável será adicionado.</span><span class="sxs-lookup"><span data-stu-id="e91fc-118">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="e91fc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e91fc-119">-Confirm</span></span>
<span data-ttu-id="e91fc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e91fc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e91fc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e91fc-121">-WhatIf</span></span>
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

### <span data-ttu-id="e91fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e91fc-122">-DefaultProfile</span></span>
<span data-ttu-id="e91fc-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e91fc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e91fc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91fc-124">CommonParameters</span></span>
<span data-ttu-id="e91fc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91fc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91fc-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e91fc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91fc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e91fc-127">INPUTS</span></span>

## <span data-ttu-id="e91fc-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e91fc-128">OUTPUTS</span></span>

### <span data-ttu-id="e91fc-129">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="e91fc-129">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="e91fc-130">O provedor de identidade confiável adicionado.</span><span class="sxs-lookup"><span data-stu-id="e91fc-130">The added Trusted Identity Provider.</span></span>

## <span data-ttu-id="e91fc-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e91fc-131">NOTES</span></span>

## <span data-ttu-id="e91fc-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e91fc-132">RELATED LINKS</span></span>
