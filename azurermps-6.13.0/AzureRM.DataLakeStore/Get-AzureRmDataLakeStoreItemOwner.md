---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 4276b9477e51165e01c716095d5f4e2a4ea6ca69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428489"
---
# <span data-ttu-id="0b522-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="0b522-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="0b522-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b522-102">SYNOPSIS</span></span>
<span data-ttu-id="0b522-103">Obtém o proprietário de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0b522-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b522-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b522-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b522-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b522-105">DESCRIPTION</span></span>
<span data-ttu-id="0b522-106">O cmdlet **Get-AzureRmDataLakeStoreItemOwner** Obtém o proprietário de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="0b522-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0b522-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b522-107">EXAMPLES</span></span>

### <span data-ttu-id="0b522-108">Exemplo 1: obter o proprietário de um diretório</span><span class="sxs-lookup"><span data-stu-id="0b522-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="0b522-109">Esse comando obtém o proprietário do usuário para o diretório raiz da conta do ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="0b522-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="0b522-110">OS</span><span class="sxs-lookup"><span data-stu-id="0b522-110">PARAMETERS</span></span>

### <span data-ttu-id="0b522-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="0b522-111">-Account</span></span>
<span data-ttu-id="0b522-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0b522-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0b522-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b522-113">-DefaultProfile</span></span>
<span data-ttu-id="0b522-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b522-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b522-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="0b522-115">-Path</span></span>
<span data-ttu-id="0b522-116">Especifica o caminho do repositório data Lake de um item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="0b522-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b522-117">-Digite</span><span class="sxs-lookup"><span data-stu-id="0b522-117">-Type</span></span>
<span data-ttu-id="0b522-118">Especifica o tipo de proprietário a obter.</span><span class="sxs-lookup"><span data-stu-id="0b522-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="0b522-119">Os valores aceitáveis para esse parâmetro são: usuário e grupo.</span><span class="sxs-lookup"><span data-stu-id="0b522-119">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b522-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b522-120">CommonParameters</span></span>
<span data-ttu-id="0b522-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b522-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b522-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b522-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b522-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b522-123">INPUTS</span></span>

### <span data-ttu-id="0b522-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0b522-124">System.String</span></span>

### <span data-ttu-id="0b522-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0b522-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0b522-126">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="0b522-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="0b522-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b522-127">OUTPUTS</span></span>

### <span data-ttu-id="0b522-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0b522-128">System.String</span></span>
<span data-ttu-id="0b522-129">O proprietário do item especificado.</span><span class="sxs-lookup"><span data-stu-id="0b522-129">The owner of the specified item.</span></span>

## <span data-ttu-id="0b522-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b522-130">NOTES</span></span>

## <span data-ttu-id="0b522-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b522-131">RELATED LINKS</span></span>

[<span data-ttu-id="0b522-132">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="0b522-132">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


