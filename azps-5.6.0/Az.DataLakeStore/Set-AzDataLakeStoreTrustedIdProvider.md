---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 7efe0e21b6b433160eab36856d3419dc918cbfc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891035"
---
# <span data-ttu-id="b2f0e-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b2f0e-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="b2f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f0e-103">Modifica o provedor de identidade confiável especificado no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b2f0e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b2f0e-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2f0e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b2f0e-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f0e-106">O cmdlet **Set-AzDataLakeStoreTrustedIdProvider** modifica o provedor de identidade confiável especificado no Repositório de Data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b2f0e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2f0e-107">EXAMPLES</span></span>

### <span data-ttu-id="b2f0e-108">Exemplo 1: atualizar um ponto de extremidade do provedor de identidade confiável</span><span class="sxs-lookup"><span data-stu-id="b2f0e-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="b2f0e-109">Isso atualiza o ponto de extremidade do provedor para a regra de firewall "MyProvider" na conta "ContosoADL" para https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 " "</span><span class="sxs-lookup"><span data-stu-id="b2f0e-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="b2f0e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b2f0e-110">PARAMETERS</span></span>

### <span data-ttu-id="b2f0e-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b2f0e-111">-Account</span></span>
<span data-ttu-id="b2f0e-112">A conta do Data Lake Store para adicionar o provedor de identidade confiável ao</span><span class="sxs-lookup"><span data-stu-id="b2f0e-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="b2f0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f0e-113">-DefaultProfile</span></span>
<span data-ttu-id="b2f0e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b2f0e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2f0e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b2f0e-115">-Name</span></span>
<span data-ttu-id="b2f0e-116">O nome do provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="b2f0e-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2f0e-117">-ProviderEndpoint</span></span>
<span data-ttu-id="b2f0e-118">O ponto de extremidade de provedor confiável válido no formato: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="b2f0e-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="b2f0e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f0e-119">-ResourceGroupName</span></span>
<span data-ttu-id="b2f0e-120">Especifica o nome do grupo de recursos que contém a conta para a atualização do provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="b2f0e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2f0e-121">-Confirm</span></span>
<span data-ttu-id="b2f0e-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f0e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f0e-123">-WhatIf</span></span>
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

### <span data-ttu-id="b2f0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f0e-124">CommonParameters</span></span>
<span data-ttu-id="b2f0e-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f0e-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f0e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f0e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2f0e-127">INPUTS</span></span>

### <span data-ttu-id="b2f0e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b2f0e-128">System.String</span></span>

## <span data-ttu-id="b2f0e-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b2f0e-129">OUTPUTS</span></span>

### <span data-ttu-id="b2f0e-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b2f0e-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="b2f0e-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="b2f0e-131">NOTES</span></span>

## <span data-ttu-id="b2f0e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2f0e-132">RELATED LINKS</span></span>
