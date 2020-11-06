---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f15ef7201622394a2b96964244980b059f1222c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426378"
---
# <span data-ttu-id="6d10a-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6d10a-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="6d10a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d10a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d10a-103">Obtém detalhes de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d10a-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d10a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d10a-104">SYNTAX</span></span>

### <span data-ttu-id="6d10a-105">GetAllInSubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d10a-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d10a-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6d10a-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d10a-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="6d10a-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d10a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d10a-108">DESCRIPTION</span></span>
<span data-ttu-id="6d10a-109">O cmdlet **Get-AzureRmDataLakeStoreAccount** Obtém detalhes de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d10a-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="6d10a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d10a-110">EXAMPLES</span></span>

### <span data-ttu-id="6d10a-111">Exemplo 1: obter uma conta do data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6d10a-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="6d10a-112">Esse comando obtém a conta chamada ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="6d10a-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="6d10a-113">OS</span><span class="sxs-lookup"><span data-stu-id="6d10a-113">PARAMETERS</span></span>

### <span data-ttu-id="6d10a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d10a-114">-DefaultProfile</span></span>
<span data-ttu-id="6d10a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6d10a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d10a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d10a-116">-Name</span></span>
<span data-ttu-id="6d10a-117">Especifica o nome da conta a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="6d10a-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d10a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d10a-118">-ResourceGroupName</span></span>
<span data-ttu-id="6d10a-119">Especifica o nome do grupo de recursos que contém a conta do data Lake Store a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="6d10a-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d10a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d10a-120">CommonParameters</span></span>
<span data-ttu-id="6d10a-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d10a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d10a-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d10a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d10a-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d10a-123">INPUTS</span></span>

### <span data-ttu-id="6d10a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6d10a-124">System.String</span></span>

## <span data-ttu-id="6d10a-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d10a-125">OUTPUTS</span></span>

### <span data-ttu-id="6d10a-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6d10a-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="6d10a-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d10a-127">NOTES</span></span>

## <span data-ttu-id="6d10a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d10a-128">RELATED LINKS</span></span>

[<span data-ttu-id="6d10a-129">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6d10a-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6d10a-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6d10a-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6d10a-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6d10a-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6d10a-132">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6d10a-132">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


