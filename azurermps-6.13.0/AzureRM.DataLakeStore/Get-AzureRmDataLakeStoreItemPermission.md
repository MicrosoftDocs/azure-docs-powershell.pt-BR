---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 6aeae8333cc8aa5a394abfaba68dcc0d7fb732f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428486"
---
# <span data-ttu-id="77619-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="77619-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="77619-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77619-102">SYNOPSIS</span></span>
<span data-ttu-id="77619-103">Obtém a permissão octal de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="77619-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77619-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77619-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77619-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77619-105">DESCRIPTION</span></span>
<span data-ttu-id="77619-106">O cmdlet **Get-AzureRmDataLakeStoreItemPermission** Obtém a permissão octal de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="77619-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="77619-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77619-107">EXAMPLES</span></span>

### <span data-ttu-id="77619-108">Exemplo 1: definir a permissão octal para um arquivo</span><span class="sxs-lookup"><span data-stu-id="77619-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="77619-109">Esse comando obtém a permissão octal de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="77619-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="77619-110">OS</span><span class="sxs-lookup"><span data-stu-id="77619-110">PARAMETERS</span></span>

### <span data-ttu-id="77619-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="77619-111">-Account</span></span>
<span data-ttu-id="77619-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="77619-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="77619-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77619-113">-DefaultProfile</span></span>
<span data-ttu-id="77619-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77619-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77619-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="77619-115">-Path</span></span>
<span data-ttu-id="77619-116">Especifica o caminho do repositório data Lake do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="77619-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="77619-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77619-117">CommonParameters</span></span>
<span data-ttu-id="77619-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77619-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77619-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77619-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77619-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77619-120">INPUTS</span></span>

### <span data-ttu-id="77619-121">System. String</span><span class="sxs-lookup"><span data-stu-id="77619-121">System.String</span></span>

### <span data-ttu-id="77619-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="77619-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="77619-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77619-123">OUTPUTS</span></span>

### <span data-ttu-id="77619-124">System. String</span><span class="sxs-lookup"><span data-stu-id="77619-124">System.String</span></span>
<span data-ttu-id="77619-125">A representação de cadeia de caracteres da propriedade octal</span><span class="sxs-lookup"><span data-stu-id="77619-125">The string representation of the ownership octal</span></span>

## <span data-ttu-id="77619-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77619-126">NOTES</span></span>
* <span data-ttu-id="77619-127">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="77619-127">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="77619-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77619-128">RELATED LINKS</span></span>

[<span data-ttu-id="77619-129">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="77619-129">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


