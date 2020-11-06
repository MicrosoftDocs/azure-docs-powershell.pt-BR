---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c05ca64db5b04ef78778e39d9ae6347db4ca05b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427940"
---
# <span data-ttu-id="e020d-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e020d-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="e020d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e020d-102">SYNOPSIS</span></span>
<span data-ttu-id="e020d-103">Obtém detalhes de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e020d-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e020d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e020d-104">SYNTAX</span></span>

### <span data-ttu-id="e020d-105">Todos na assinatura (padrão)</span><span class="sxs-lookup"><span data-stu-id="e020d-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e020d-106">Tudo no grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e020d-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e020d-107">Conta específica</span><span class="sxs-lookup"><span data-stu-id="e020d-107">Specific Account</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e020d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e020d-108">DESCRIPTION</span></span>
<span data-ttu-id="e020d-109">O cmdlet **Get-AzureRmDataLakeStoreAccount** Obtém detalhes de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e020d-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="e020d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e020d-110">EXAMPLES</span></span>

### <span data-ttu-id="e020d-111">Exemplo 1: obter uma conta do data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e020d-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="e020d-112">Esse comando obtém a conta chamada ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="e020d-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="e020d-113">OS</span><span class="sxs-lookup"><span data-stu-id="e020d-113">PARAMETERS</span></span>

### <span data-ttu-id="e020d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e020d-114">-Name</span></span>
<span data-ttu-id="e020d-115">Especifica o nome da conta a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="e020d-115">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e020d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e020d-116">-ResourceGroupName</span></span>
<span data-ttu-id="e020d-117">Especifica o nome do grupo de recursos que contém a conta do data Lake Store a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="e020d-117">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e020d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e020d-118">-DefaultProfile</span></span>
<span data-ttu-id="e020d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e020d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e020d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e020d-120">CommonParameters</span></span>
<span data-ttu-id="e020d-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e020d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e020d-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e020d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e020d-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e020d-123">INPUTS</span></span>

## <span data-ttu-id="e020d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e020d-124">OUTPUTS</span></span>

### <span data-ttu-id="e020d-125">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e020d-125">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="e020d-126">A conta específica do data Lake Store solicitada.</span><span class="sxs-lookup"><span data-stu-id="e020d-126">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="e020d-127">Programação<PSDataLakeStoreAccount></span><span class="sxs-lookup"><span data-stu-id="e020d-127">List<PSDataLakeStoreAccount></span></span>
<span data-ttu-id="e020d-128">Uma lista de contas do data Lake Store no grupo de recursos ou na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="e020d-128">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="e020d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e020d-129">NOTES</span></span>

## <span data-ttu-id="e020d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e020d-130">RELATED LINKS</span></span>

[<span data-ttu-id="e020d-131">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e020d-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="e020d-132">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e020d-132">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="e020d-133">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e020d-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="e020d-134">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e020d-134">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


