---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 64af120d793719d4bcd6a24cc3d480cc8f6c104f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601070"
---
# <span data-ttu-id="035a0-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="035a0-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="035a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="035a0-102">SYNOPSIS</span></span>
<span data-ttu-id="035a0-103">Obtém o proprietário de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="035a0-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="035a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="035a0-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="035a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="035a0-105">DESCRIPTION</span></span>
<span data-ttu-id="035a0-106">O cmdlet **Get-AzDataLakeStoreItemOwner** Obtém o proprietário de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="035a0-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="035a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="035a0-107">EXAMPLES</span></span>

### <span data-ttu-id="035a0-108">Exemplo 1: obter o proprietário de um diretório</span><span class="sxs-lookup"><span data-stu-id="035a0-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="035a0-109">Esse comando obtém o proprietário do usuário para o diretório raiz da conta do ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="035a0-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="035a0-110">OS</span><span class="sxs-lookup"><span data-stu-id="035a0-110">PARAMETERS</span></span>

### <span data-ttu-id="035a0-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="035a0-111">-Account</span></span>
<span data-ttu-id="035a0-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="035a0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="035a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035a0-113">-DefaultProfile</span></span>
<span data-ttu-id="035a0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="035a0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="035a0-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="035a0-115">-Path</span></span>
<span data-ttu-id="035a0-116">Especifica o caminho do repositório data Lake de um item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="035a0-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="035a0-117">-Digite</span><span class="sxs-lookup"><span data-stu-id="035a0-117">-Type</span></span>
<span data-ttu-id="035a0-118">Especifica o tipo de proprietário a obter.</span><span class="sxs-lookup"><span data-stu-id="035a0-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="035a0-119">Os valores aceitáveis para esse parâmetro são: usuário e grupo.</span><span class="sxs-lookup"><span data-stu-id="035a0-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="035a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035a0-120">CommonParameters</span></span>
<span data-ttu-id="035a0-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="035a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035a0-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="035a0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035a0-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="035a0-123">INPUTS</span></span>

### <span data-ttu-id="035a0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="035a0-124">System.String</span></span>

### <span data-ttu-id="035a0-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="035a0-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="035a0-126">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="035a0-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="035a0-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="035a0-127">OUTPUTS</span></span>

### <span data-ttu-id="035a0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="035a0-128">System.String</span></span>

## <span data-ttu-id="035a0-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="035a0-129">NOTES</span></span>

## <span data-ttu-id="035a0-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="035a0-130">RELATED LINKS</span></span>

[<span data-ttu-id="035a0-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="035a0-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


