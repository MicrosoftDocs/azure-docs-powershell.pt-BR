---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 61899a50c857fc3e8852d362d5905b0ca2fedf6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431693"
---
# <span data-ttu-id="5e327-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5e327-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="5e327-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e327-102">SYNOPSIS</span></span>
<span data-ttu-id="5e327-103">Obtém detalhes de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5e327-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e327-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e327-104">SYNTAX</span></span>

### <span data-ttu-id="5e327-105">GetAllInSubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e327-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e327-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e327-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e327-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="5e327-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e327-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e327-108">DESCRIPTION</span></span>
<span data-ttu-id="5e327-109">O cmdlet **Get-AzureRmDataLakeStoreAccount** Obtém detalhes de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5e327-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="5e327-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e327-110">EXAMPLES</span></span>

### <span data-ttu-id="5e327-111">Exemplo 1: obter uma conta do data Lake Store</span><span class="sxs-lookup"><span data-stu-id="5e327-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="5e327-112">Esse comando obtém a conta chamada ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="5e327-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="5e327-113">OS</span><span class="sxs-lookup"><span data-stu-id="5e327-113">PARAMETERS</span></span>

### <span data-ttu-id="5e327-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e327-114">-DefaultProfile</span></span>
<span data-ttu-id="5e327-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5e327-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e327-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e327-116">-Name</span></span>
<span data-ttu-id="5e327-117">Especifica o nome da conta a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="5e327-117">Specifies the name of the account to get.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e327-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e327-118">-ResourceGroupName</span></span>
<span data-ttu-id="5e327-119">Especifica o nome do grupo de recursos que contém a conta do data Lake Store a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="5e327-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e327-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e327-120">CommonParameters</span></span>
<span data-ttu-id="5e327-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e327-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e327-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e327-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e327-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e327-123">INPUTS</span></span>

### <span data-ttu-id="5e327-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5e327-124">None</span></span>
<span data-ttu-id="5e327-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5e327-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e327-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e327-126">OUTPUTS</span></span>

### <span data-ttu-id="5e327-127">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5e327-127">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="5e327-128">A conta específica do data Lake Store solicitada.</span><span class="sxs-lookup"><span data-stu-id="5e327-128">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="5e327-129">Programação<PSDataLakeStoreAccountBasic></span><span class="sxs-lookup"><span data-stu-id="5e327-129">List<PSDataLakeStoreAccountBasic></span></span>
<span data-ttu-id="5e327-130">Uma lista de contas do data Lake Store no grupo de recursos ou na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="5e327-130">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="5e327-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e327-131">NOTES</span></span>

## <span data-ttu-id="5e327-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e327-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e327-133">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5e327-133">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="5e327-134">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5e327-134">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="5e327-135">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5e327-135">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="5e327-136">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5e327-136">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


