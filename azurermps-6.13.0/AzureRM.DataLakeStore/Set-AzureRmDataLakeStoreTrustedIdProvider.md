---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 509c80f77d48cebd101703727cefb37399ed2577
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429571"
---
# <span data-ttu-id="73783-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="73783-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="73783-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73783-102">SYNOPSIS</span></span>
<span data-ttu-id="73783-103">Modifica o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="73783-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73783-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73783-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73783-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73783-105">DESCRIPTION</span></span>
<span data-ttu-id="73783-106">O cmdlet **set-AzureRmDataLakeStoreTrustedIdProvider** modifica o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="73783-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="73783-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73783-107">EXAMPLES</span></span>

### <span data-ttu-id="73783-108">Exemplo 1: atualizar um ponto de extremidade do provedor de identidade confiável</span><span class="sxs-lookup"><span data-stu-id="73783-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="73783-109">Isso atualiza o provedor endpoing para a regra de firewall "MyProvider" na conta "ContosoADL" para " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="73783-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="73783-110">OS</span><span class="sxs-lookup"><span data-stu-id="73783-110">PARAMETERS</span></span>

### <span data-ttu-id="73783-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="73783-111">-Account</span></span>
<span data-ttu-id="73783-112">A conta do data Lake Store para adicionar o provedor de identidade confiável</span><span class="sxs-lookup"><span data-stu-id="73783-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="73783-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73783-113">-DefaultProfile</span></span>
<span data-ttu-id="73783-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="73783-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73783-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="73783-115">-Name</span></span>
<span data-ttu-id="73783-116">O nome do provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="73783-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="73783-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="73783-117">-ProviderEndpoint</span></span>
<span data-ttu-id="73783-118">O ponto de extremidade do provedor confiável válido no formato: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="73783-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="73783-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73783-119">-ResourceGroupName</span></span>
<span data-ttu-id="73783-120">Especifica o nome do grupo de recursos que contém a conta para a qual atualizar o provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="73783-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="73783-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="73783-121">-Confirm</span></span>
<span data-ttu-id="73783-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73783-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73783-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73783-123">-WhatIf</span></span>
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

### <span data-ttu-id="73783-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73783-124">CommonParameters</span></span>
<span data-ttu-id="73783-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73783-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73783-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73783-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73783-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73783-127">INPUTS</span></span>

### <span data-ttu-id="73783-128">System. String</span><span class="sxs-lookup"><span data-stu-id="73783-128">System.String</span></span>

## <span data-ttu-id="73783-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73783-129">OUTPUTS</span></span>

### <span data-ttu-id="73783-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="73783-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="73783-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73783-131">NOTES</span></span>

## <span data-ttu-id="73783-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73783-132">RELATED LINKS</span></span>
