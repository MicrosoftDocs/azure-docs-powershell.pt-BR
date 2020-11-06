---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: f76473239661b492c95a356dfb1b381e1093f98c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428934"
---
# <span data-ttu-id="09b77-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="09b77-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="09b77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09b77-102">SYNOPSIS</span></span>
<span data-ttu-id="09b77-103">Obtém a permissão octal de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="09b77-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09b77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09b77-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09b77-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09b77-105">DESCRIPTION</span></span>
<span data-ttu-id="09b77-106">O cmdlet **Get-AzureRmDataLakeStoreItemPermission** Obtém a permissão octal de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="09b77-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="09b77-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09b77-107">EXAMPLES</span></span>

### <span data-ttu-id="09b77-108">Exemplo 1: definir a permissão octal para um arquivo</span><span class="sxs-lookup"><span data-stu-id="09b77-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="09b77-109">Esse comando obtém a permissão octal de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="09b77-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="09b77-110">OS</span><span class="sxs-lookup"><span data-stu-id="09b77-110">PARAMETERS</span></span>

### <span data-ttu-id="09b77-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="09b77-111">-Account</span></span>
<span data-ttu-id="09b77-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="09b77-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b77-113">-DefaultProfile</span></span>
<span data-ttu-id="09b77-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09b77-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09b77-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="09b77-115">-Path</span></span>
<span data-ttu-id="09b77-116">Especifica o caminho do repositório data Lake do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="09b77-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b77-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b77-117">CommonParameters</span></span>
<span data-ttu-id="09b77-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09b77-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b77-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09b77-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b77-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09b77-120">INPUTS</span></span>

### <span data-ttu-id="09b77-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="09b77-121">None</span></span>
<span data-ttu-id="09b77-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="09b77-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09b77-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09b77-123">OUTPUTS</span></span>

### <span data-ttu-id="09b77-124">String</span><span class="sxs-lookup"><span data-stu-id="09b77-124">string</span></span>
<span data-ttu-id="09b77-125">A representação de cadeia de caracteres da propriedade octal</span><span class="sxs-lookup"><span data-stu-id="09b77-125">The string representation of the ownership octal</span></span>

## <span data-ttu-id="09b77-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09b77-126">NOTES</span></span>
* <span data-ttu-id="09b77-127">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="09b77-127">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="09b77-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09b77-128">RELATED LINKS</span></span>

[<span data-ttu-id="09b77-129">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="09b77-129">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


