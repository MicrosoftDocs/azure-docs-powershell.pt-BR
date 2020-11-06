---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: e95fd5e487fc29a40e48484b0a905def8356e260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433149"
---
# <span data-ttu-id="ceecc-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="ceecc-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="ceecc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ceecc-102">SYNOPSIS</span></span>
<span data-ttu-id="ceecc-103">Obtém o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="ceecc-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="ceecc-104">Se nenhum provedor for especificado, lista todos os provedores da conta.</span><span class="sxs-lookup"><span data-stu-id="ceecc-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceecc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ceecc-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceecc-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ceecc-106">DESCRIPTION</span></span>
<span data-ttu-id="ceecc-107">O cmdlet **Get-AzureRmDataLakeStoreTrustedIdProvider** Obtém o provedor de identidade confiável especificado no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="ceecc-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="ceecc-108">Se nenhum provedor for especificado, lista todos os provedores da conta.</span><span class="sxs-lookup"><span data-stu-id="ceecc-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="ceecc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ceecc-109">EXAMPLES</span></span>

### <span data-ttu-id="ceecc-110">Exemplo 1: obter um provedor de identidade confiável específico</span><span class="sxs-lookup"><span data-stu-id="ceecc-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="ceecc-111">Retorna o provedor chamado "MyProvider" da conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="ceecc-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="ceecc-112">Exemplo 2: listar todos os provedores em uma conta</span><span class="sxs-lookup"><span data-stu-id="ceecc-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="ceecc-113">Lista todos os provedores na conta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="ceecc-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="ceecc-114">OS</span><span class="sxs-lookup"><span data-stu-id="ceecc-114">PARAMETERS</span></span>

### <span data-ttu-id="ceecc-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="ceecc-115">-Account</span></span>
<span data-ttu-id="ceecc-116">A conta do data Lake Store para recuperar o provedor de identidade confiável do</span><span class="sxs-lookup"><span data-stu-id="ceecc-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="ceecc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ceecc-117">-Name</span></span>
<span data-ttu-id="ceecc-118">O nome do provedor de identidade confiável a ser recuperado</span><span class="sxs-lookup"><span data-stu-id="ceecc-118">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="ceecc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceecc-119">-ResourceGroupName</span></span>
<span data-ttu-id="ceecc-120">Nome do grupo de recursos sob o qual deseja recuperar o provedor de identidade confiável especificado da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="ceecc-120">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="ceecc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceecc-121">-DefaultProfile</span></span>
<span data-ttu-id="ceecc-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ceecc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceecc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceecc-123">CommonParameters</span></span>
<span data-ttu-id="ceecc-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceecc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceecc-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceecc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceecc-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ceecc-126">INPUTS</span></span>

## <span data-ttu-id="ceecc-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ceecc-127">OUTPUTS</span></span>

### <span data-ttu-id="ceecc-128">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="ceecc-128">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="ceecc-129">Os detalhes do provedor de identidade confiável especificado.</span><span class="sxs-lookup"><span data-stu-id="ceecc-129">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="ceecc-130">IList<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="ceecc-130">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="ceecc-131">A lista de provedores de identidade confiáveis na conta especificada.</span><span class="sxs-lookup"><span data-stu-id="ceecc-131">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="ceecc-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ceecc-132">NOTES</span></span>

## <span data-ttu-id="ceecc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ceecc-133">RELATED LINKS</span></span>

