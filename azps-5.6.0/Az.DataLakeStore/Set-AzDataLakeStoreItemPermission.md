---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 7294d5c48bd8cbc94ac127ac1f1543827dc2937b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891037"
---
# <span data-ttu-id="52f17-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="52f17-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="52f17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52f17-102">SYNOPSIS</span></span>
<span data-ttu-id="52f17-103">Modifica o octal de permissão de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="52f17-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="52f17-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52f17-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52f17-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52f17-105">DESCRIPTION</span></span>
<span data-ttu-id="52f17-106">O cmdlet **Set-AzDataLakeStoreItemPermission** modifica o octal de permissão de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="52f17-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="52f17-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52f17-107">EXAMPLES</span></span>

### <span data-ttu-id="52f17-108">Exemplo 1: definir o octal de permissão para um item</span><span class="sxs-lookup"><span data-stu-id="52f17-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="52f17-109">Este comando define o octal de permissão para um arquivo como 0770, que se traduz em limpar o bit grudado, definindo permissões de leitura/gravação/execução para o proprietário do arquivo, definindo permissões de leitura/gravação/execução para o grupo proprietário do arquivo e limpando permissões de leitura/gravação/execução para outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="52f17-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="52f17-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52f17-110">PARAMETERS</span></span>

### <span data-ttu-id="52f17-111">-Account</span><span class="sxs-lookup"><span data-stu-id="52f17-111">-Account</span></span>
<span data-ttu-id="52f17-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="52f17-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="52f17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f17-113">-DefaultProfile</span></span>
<span data-ttu-id="52f17-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="52f17-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52f17-115">-Path</span><span class="sxs-lookup"><span data-stu-id="52f17-115">-Path</span></span>
<span data-ttu-id="52f17-116">Especifica o caminho do Data Lake Store do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="52f17-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="52f17-117">-Permission</span><span class="sxs-lookup"><span data-stu-id="52f17-117">-Permission</span></span>
<span data-ttu-id="52f17-118">As permissões a definir para o arquivo ou pasta, expressas como uma octal (por exemplo, '777')</span><span class="sxs-lookup"><span data-stu-id="52f17-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f17-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52f17-119">-Confirm</span></span>
<span data-ttu-id="52f17-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52f17-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f17-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52f17-121">-WhatIf</span></span>
<span data-ttu-id="52f17-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52f17-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52f17-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52f17-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f17-124">CommonParameters</span></span>
<span data-ttu-id="52f17-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f17-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f17-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f17-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52f17-127">INPUTS</span></span>

### <span data-ttu-id="52f17-128">System.String</span><span class="sxs-lookup"><span data-stu-id="52f17-128">System.String</span></span>

### <span data-ttu-id="52f17-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="52f17-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="52f17-130">System.Int32</span><span class="sxs-lookup"><span data-stu-id="52f17-130">System.Int32</span></span>

## <span data-ttu-id="52f17-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52f17-131">OUTPUTS</span></span>

### <span data-ttu-id="52f17-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52f17-132">System.Boolean</span></span>

## <span data-ttu-id="52f17-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="52f17-133">NOTES</span></span>
* <span data-ttu-id="52f17-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="52f17-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="52f17-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52f17-135">RELATED LINKS</span></span>

[<span data-ttu-id="52f17-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="52f17-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


