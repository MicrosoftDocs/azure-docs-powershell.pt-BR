---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 5c36257050cccf217234a3b1ef6b89120e36b3c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609694"
---
# <span data-ttu-id="e8adc-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="e8adc-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="e8adc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8adc-102">SYNOPSIS</span></span>
<span data-ttu-id="e8adc-103">Obtém o proprietário de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e8adc-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8adc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8adc-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8adc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8adc-105">DESCRIPTION</span></span>
<span data-ttu-id="e8adc-106">O cmdlet **Get-AzureRmDataLakeStoreItemOwner** Obtém o proprietário de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="e8adc-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e8adc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8adc-107">EXAMPLES</span></span>

### <span data-ttu-id="e8adc-108">Exemplo 1: obter o proprietário de um diretório</span><span class="sxs-lookup"><span data-stu-id="e8adc-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="e8adc-109">Esse comando obtém o proprietário do usuário para o diretório raiz da conta do ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="e8adc-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="e8adc-110">OS</span><span class="sxs-lookup"><span data-stu-id="e8adc-110">PARAMETERS</span></span>

### <span data-ttu-id="e8adc-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="e8adc-111">-Account</span></span>
<span data-ttu-id="e8adc-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e8adc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e8adc-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="e8adc-113">-Path</span></span>
<span data-ttu-id="e8adc-114">Especifica o caminho do repositório data Lake de um item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="e8adc-114">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e8adc-115">-Digite</span><span class="sxs-lookup"><span data-stu-id="e8adc-115">-Type</span></span>
<span data-ttu-id="e8adc-116">Especifica o tipo de proprietário a obter.</span><span class="sxs-lookup"><span data-stu-id="e8adc-116">Specifies the type of owner to get.</span></span>
<span data-ttu-id="e8adc-117">Os valores aceitáveis para esse parâmetro são: usuário e grupo.</span><span class="sxs-lookup"><span data-stu-id="e8adc-117">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="e8adc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8adc-118">-DefaultProfile</span></span>
<span data-ttu-id="e8adc-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8adc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8adc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8adc-120">CommonParameters</span></span>
<span data-ttu-id="e8adc-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8adc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8adc-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8adc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8adc-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8adc-123">INPUTS</span></span>

## <span data-ttu-id="e8adc-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8adc-124">OUTPUTS</span></span>

### <span data-ttu-id="e8adc-125">String</span><span class="sxs-lookup"><span data-stu-id="e8adc-125">string</span></span>
<span data-ttu-id="e8adc-126">O proprietário do item especificado.</span><span class="sxs-lookup"><span data-stu-id="e8adc-126">The owner of the specified item.</span></span>

## <span data-ttu-id="e8adc-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8adc-127">NOTES</span></span>

## <span data-ttu-id="e8adc-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8adc-128">RELATED LINKS</span></span>

[<span data-ttu-id="e8adc-129">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="e8adc-129">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


