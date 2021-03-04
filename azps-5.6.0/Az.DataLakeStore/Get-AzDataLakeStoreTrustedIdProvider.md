---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: ac03d161e8ea786b939f8068dc2efd9109af3ab5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887779"
---
# <span data-ttu-id="1dc57-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="1dc57-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="1dc57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dc57-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc57-103">Obtém o provedor de identidade confiável especificado no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="1dc57-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="1dc57-104">Se nenhum provedor for especificado, lista todos os provedores da conta.</span><span class="sxs-lookup"><span data-stu-id="1dc57-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="1dc57-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1dc57-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dc57-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1dc57-106">DESCRIPTION</span></span>
<span data-ttu-id="1dc57-107">O cmdlet **Get-AzDataLakeStoreTrustedIdProvider** obtém o provedor de identidade confiável especificado no Repositório de Data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="1dc57-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="1dc57-108">Se nenhum provedor for especificado, lista todos os provedores da conta.</span><span class="sxs-lookup"><span data-stu-id="1dc57-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="1dc57-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dc57-109">EXAMPLES</span></span>

### <span data-ttu-id="1dc57-110">Exemplo 1: Obter um provedor de identidade confiável específico</span><span class="sxs-lookup"><span data-stu-id="1dc57-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="1dc57-111">Retorna o provedor chamado "MyProvider" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="1dc57-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="1dc57-112">Exemplo 2: Listar todos os provedores em uma conta</span><span class="sxs-lookup"><span data-stu-id="1dc57-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="1dc57-113">Lista todos os provedores na conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="1dc57-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="1dc57-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1dc57-114">PARAMETERS</span></span>

### <span data-ttu-id="1dc57-115">-Account</span><span class="sxs-lookup"><span data-stu-id="1dc57-115">-Account</span></span>
<span data-ttu-id="1dc57-116">A conta do Data Lake Store para recuperar o provedor de identidade confiável de</span><span class="sxs-lookup"><span data-stu-id="1dc57-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="1dc57-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc57-117">-DefaultProfile</span></span>
<span data-ttu-id="1dc57-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1dc57-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dc57-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1dc57-119">-Name</span></span>
<span data-ttu-id="1dc57-120">O nome do provedor de identidade confiável a ser recuperado</span><span class="sxs-lookup"><span data-stu-id="1dc57-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc57-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc57-121">-ResourceGroupName</span></span>
<span data-ttu-id="1dc57-122">Nome do grupo de recursos no qual deseja recuperar o provedor de identidade confiável especificado da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="1dc57-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc57-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc57-123">CommonParameters</span></span>
<span data-ttu-id="1dc57-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc57-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc57-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc57-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc57-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1dc57-126">INPUTS</span></span>

### <span data-ttu-id="1dc57-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1dc57-127">System.String</span></span>

## <span data-ttu-id="1dc57-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1dc57-128">OUTPUTS</span></span>

### <span data-ttu-id="1dc57-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="1dc57-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="1dc57-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="1dc57-130">NOTES</span></span>

## <span data-ttu-id="1dc57-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dc57-131">RELATED LINKS</span></span>
