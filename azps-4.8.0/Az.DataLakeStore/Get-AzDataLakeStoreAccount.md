---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111132"
---
# <span data-ttu-id="64112-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="64112-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="64112-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64112-102">SYNOPSIS</span></span>
<span data-ttu-id="64112-103">Obtém detalhes de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="64112-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="64112-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64112-104">SYNTAX</span></span>

### <span data-ttu-id="64112-105">GetAllInSubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="64112-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64112-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="64112-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64112-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="64112-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64112-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64112-108">DESCRIPTION</span></span>
<span data-ttu-id="64112-109">O cmdlet **Get-AzDataLakeStoreAccount** Obtém detalhes de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="64112-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="64112-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64112-110">EXAMPLES</span></span>

### <span data-ttu-id="64112-111">Exemplo 1: obter uma conta do data Lake Store</span><span class="sxs-lookup"><span data-stu-id="64112-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="64112-112">Esse comando obtém a conta chamada ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="64112-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="64112-113">OS</span><span class="sxs-lookup"><span data-stu-id="64112-113">PARAMETERS</span></span>

### <span data-ttu-id="64112-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64112-114">-DefaultProfile</span></span>
<span data-ttu-id="64112-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="64112-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64112-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="64112-116">-Name</span></span>
<span data-ttu-id="64112-117">Especifica o nome da conta a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="64112-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="64112-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64112-118">-ResourceGroupName</span></span>
<span data-ttu-id="64112-119">Especifica o nome do grupo de recursos que contém a conta do data Lake Store a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="64112-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="64112-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64112-120">CommonParameters</span></span>
<span data-ttu-id="64112-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64112-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64112-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64112-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64112-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64112-123">INPUTS</span></span>

### <span data-ttu-id="64112-124">System. String</span><span class="sxs-lookup"><span data-stu-id="64112-124">System.String</span></span>

## <span data-ttu-id="64112-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64112-125">OUTPUTS</span></span>

### <span data-ttu-id="64112-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="64112-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="64112-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64112-127">NOTES</span></span>

## <span data-ttu-id="64112-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64112-128">RELATED LINKS</span></span>

[<span data-ttu-id="64112-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="64112-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="64112-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="64112-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="64112-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="64112-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="64112-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="64112-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


