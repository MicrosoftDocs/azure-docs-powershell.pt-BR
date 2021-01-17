---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c4de7a926e4095ad8bb45a25647305617988330d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426585"
---
# <span data-ttu-id="c7ffe-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="c7ffe-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="c7ffe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ffe-103">Modifica o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="c7ffe-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="c7ffe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7ffe-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7ffe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="c7ffe-106">O cmdlet **set-AzDataLakeStoreTrustedIdProvider** modifica o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="c7ffe-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="c7ffe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7ffe-107">EXAMPLES</span></span>

### <span data-ttu-id="c7ffe-108">Exemplo 1: atualizar um ponto de extremidade do provedor de identidade confiável</span><span class="sxs-lookup"><span data-stu-id="c7ffe-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="c7ffe-109">Isso atualiza o ponto de extremidade do provedor para a regra de firewall "MyProvider" na conta "ContosoADL" para " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="c7ffe-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="c7ffe-110">OS</span><span class="sxs-lookup"><span data-stu-id="c7ffe-110">PARAMETERS</span></span>

### <span data-ttu-id="c7ffe-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="c7ffe-111">-Account</span></span>
<span data-ttu-id="c7ffe-112">A conta do data Lake Store para adicionar o provedor de identidade confiável</span><span class="sxs-lookup"><span data-stu-id="c7ffe-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="c7ffe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7ffe-113">-DefaultProfile</span></span>
<span data-ttu-id="c7ffe-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c7ffe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7ffe-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7ffe-115">-Name</span></span>
<span data-ttu-id="c7ffe-116">O nome do provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="c7ffe-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="c7ffe-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7ffe-117">-ProviderEndpoint</span></span>
<span data-ttu-id="c7ffe-118">O ponto de extremidade do provedor confiável válido no formato: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="c7ffe-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="c7ffe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7ffe-119">-ResourceGroupName</span></span>
<span data-ttu-id="c7ffe-120">Especifica o nome do grupo de recursos que contém a conta para a qual atualizar o provedor de identidade confiável.</span><span class="sxs-lookup"><span data-stu-id="c7ffe-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="c7ffe-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c7ffe-121">-Confirm</span></span>
<span data-ttu-id="c7ffe-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7ffe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7ffe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7ffe-123">-WhatIf</span></span>
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

### <span data-ttu-id="c7ffe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ffe-124">CommonParameters</span></span>
<span data-ttu-id="c7ffe-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7ffe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ffe-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7ffe-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ffe-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7ffe-127">INPUTS</span></span>

### <span data-ttu-id="c7ffe-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c7ffe-128">System.String</span></span>

## <span data-ttu-id="c7ffe-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7ffe-129">OUTPUTS</span></span>

### <span data-ttu-id="c7ffe-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="c7ffe-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="c7ffe-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7ffe-131">NOTES</span></span>

## <span data-ttu-id="c7ffe-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7ffe-132">RELATED LINKS</span></span>
