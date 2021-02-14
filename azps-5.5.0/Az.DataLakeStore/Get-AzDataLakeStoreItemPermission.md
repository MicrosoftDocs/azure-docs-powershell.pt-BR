---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110990"
---
# <span data-ttu-id="40c84-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="40c84-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="40c84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40c84-102">SYNOPSIS</span></span>
<span data-ttu-id="40c84-103">Obtém a permissão octal de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="40c84-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="40c84-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40c84-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40c84-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="40c84-105">DESCRIPTION</span></span>
<span data-ttu-id="40c84-106">O cmdlet **Get-AzDataLakeStoreItemPermission obtém** a octal de permissão de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="40c84-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="40c84-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="40c84-107">EXAMPLES</span></span>

### <span data-ttu-id="40c84-108">Exemplo 1: Definir a octal de permissão para um arquivo</span><span class="sxs-lookup"><span data-stu-id="40c84-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="40c84-109">Esse comando obtém a permissão octal de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="40c84-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="40c84-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40c84-110">PARAMETERS</span></span>

### <span data-ttu-id="40c84-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="40c84-111">-Account</span></span>
<span data-ttu-id="40c84-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="40c84-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="40c84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c84-113">-DefaultProfile</span></span>
<span data-ttu-id="40c84-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="40c84-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40c84-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="40c84-115">-Path</span></span>
<span data-ttu-id="40c84-116">Especifica o caminho do Data Lake Store do arquivo ou pasta, começando pelo diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="40c84-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="40c84-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c84-117">CommonParameters</span></span>
<span data-ttu-id="40c84-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40c84-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c84-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40c84-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c84-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="40c84-120">INPUTS</span></span>

### <span data-ttu-id="40c84-121">System.String</span><span class="sxs-lookup"><span data-stu-id="40c84-121">System.String</span></span>

### <span data-ttu-id="40c84-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="40c84-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="40c84-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="40c84-123">OUTPUTS</span></span>

### <span data-ttu-id="40c84-124">System.String</span><span class="sxs-lookup"><span data-stu-id="40c84-124">System.String</span></span>

## <span data-ttu-id="40c84-125">Notas</span><span class="sxs-lookup"><span data-stu-id="40c84-125">NOTES</span></span>
* <span data-ttu-id="40c84-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="40c84-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="40c84-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40c84-127">RELATED LINKS</span></span>

[<span data-ttu-id="40c84-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="40c84-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


