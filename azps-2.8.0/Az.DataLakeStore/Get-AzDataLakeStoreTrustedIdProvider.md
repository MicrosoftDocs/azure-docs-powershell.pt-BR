---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: d075c6792134536be84643d51f37b2379b63d5e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596842"
---
# <span data-ttu-id="8fc73-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="8fc73-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="8fc73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8fc73-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc73-103">Obtém o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="8fc73-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="8fc73-104">Se nenhum provedor for especificado, lista todos os provedores da conta.</span><span class="sxs-lookup"><span data-stu-id="8fc73-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="8fc73-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fc73-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fc73-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8fc73-106">DESCRIPTION</span></span>
<span data-ttu-id="8fc73-107">O cmdlet **Get-AzDataLakeStoreTrustedIdProvider** Obtém o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="8fc73-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="8fc73-108">Se nenhum provedor for especificado, lista todos os provedores da conta.</span><span class="sxs-lookup"><span data-stu-id="8fc73-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="8fc73-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fc73-109">EXAMPLES</span></span>

### <span data-ttu-id="8fc73-110">Exemplo 1: obter um provedor de identidade confiável específico</span><span class="sxs-lookup"><span data-stu-id="8fc73-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="8fc73-111">Retorna o provedor chamado "MyProvider" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="8fc73-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="8fc73-112">Exemplo 2: listar todos os provedores em uma conta</span><span class="sxs-lookup"><span data-stu-id="8fc73-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="8fc73-113">Lista todos os provedores na conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="8fc73-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="8fc73-114">OS</span><span class="sxs-lookup"><span data-stu-id="8fc73-114">PARAMETERS</span></span>

### <span data-ttu-id="8fc73-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="8fc73-115">-Account</span></span>
<span data-ttu-id="8fc73-116">A conta do data Lake Store para recuperar o provedor de identidade confiável do</span><span class="sxs-lookup"><span data-stu-id="8fc73-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="8fc73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc73-117">-DefaultProfile</span></span>
<span data-ttu-id="8fc73-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8fc73-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fc73-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fc73-119">-Name</span></span>
<span data-ttu-id="8fc73-120">O nome do provedor de identidade confiável a ser recuperado</span><span class="sxs-lookup"><span data-stu-id="8fc73-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="8fc73-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc73-121">-ResourceGroupName</span></span>
<span data-ttu-id="8fc73-122">Nome do grupo de recursos sob o qual deseja recuperar o provedor de identidade confiável especificado da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="8fc73-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="8fc73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc73-123">CommonParameters</span></span>
<span data-ttu-id="8fc73-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fc73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc73-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fc73-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc73-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8fc73-126">INPUTS</span></span>

### <span data-ttu-id="8fc73-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8fc73-127">System.String</span></span>

## <span data-ttu-id="8fc73-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8fc73-128">OUTPUTS</span></span>

### <span data-ttu-id="8fc73-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="8fc73-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="8fc73-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8fc73-130">NOTES</span></span>

## <span data-ttu-id="8fc73-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fc73-131">RELATED LINKS</span></span>
