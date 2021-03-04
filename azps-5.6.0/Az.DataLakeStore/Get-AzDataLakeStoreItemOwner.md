---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 654703a3c5cf1fc18e0f8fbb227b608e91c379bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889783"
---
# <span data-ttu-id="93032-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="93032-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="93032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93032-102">SYNOPSIS</span></span>
<span data-ttu-id="93032-103">Obtém o proprietário de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93032-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="93032-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="93032-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93032-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93032-105">DESCRIPTION</span></span>
<span data-ttu-id="93032-106">O cmdlet **Get-AzDataLakeStoreItemOwner** obtém o proprietário de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93032-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="93032-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93032-107">EXAMPLES</span></span>

### <span data-ttu-id="93032-108">Exemplo 1: Obter o proprietário de um diretório</span><span class="sxs-lookup"><span data-stu-id="93032-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="93032-109">Este comando obtém o proprietário do usuário para o diretório raiz da conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="93032-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="93032-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="93032-110">PARAMETERS</span></span>

### <span data-ttu-id="93032-111">-Account</span><span class="sxs-lookup"><span data-stu-id="93032-111">-Account</span></span>
<span data-ttu-id="93032-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93032-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="93032-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93032-113">-DefaultProfile</span></span>
<span data-ttu-id="93032-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="93032-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93032-115">-Path</span><span class="sxs-lookup"><span data-stu-id="93032-115">-Path</span></span>
<span data-ttu-id="93032-116">Especifica o caminho do Data Lake Store de um item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="93032-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="93032-117">-Type</span><span class="sxs-lookup"><span data-stu-id="93032-117">-Type</span></span>
<span data-ttu-id="93032-118">Especifica o tipo de proprietário a ser obter.</span><span class="sxs-lookup"><span data-stu-id="93032-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="93032-119">Os valores aceitáveis para este parâmetro são: Usuário e Grupo.</span><span class="sxs-lookup"><span data-stu-id="93032-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="93032-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93032-120">CommonParameters</span></span>
<span data-ttu-id="93032-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93032-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93032-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93032-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93032-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93032-123">INPUTS</span></span>

### <span data-ttu-id="93032-124">System.String</span><span class="sxs-lookup"><span data-stu-id="93032-124">System.String</span></span>

### <span data-ttu-id="93032-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="93032-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="93032-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="93032-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="93032-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="93032-127">OUTPUTS</span></span>

### <span data-ttu-id="93032-128">System.String</span><span class="sxs-lookup"><span data-stu-id="93032-128">System.String</span></span>

## <span data-ttu-id="93032-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="93032-129">NOTES</span></span>

## <span data-ttu-id="93032-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93032-130">RELATED LINKS</span></span>

[<span data-ttu-id="93032-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="93032-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


