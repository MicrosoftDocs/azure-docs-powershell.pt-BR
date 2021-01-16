---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: af14588394a94e771c1287081aa263a7ba8e9da1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262078"
---
# <span data-ttu-id="030d3-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="030d3-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="030d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="030d3-102">SYNOPSIS</span></span>
<span data-ttu-id="030d3-103">Modifica a permissão octal de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="030d3-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="030d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="030d3-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="030d3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="030d3-105">DESCRIPTION</span></span>
<span data-ttu-id="030d3-106">O cmdlet **set-AzDataLakeStoreItemPermission** modifica a permissão octal de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="030d3-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="030d3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="030d3-107">EXAMPLES</span></span>

### <span data-ttu-id="030d3-108">Exemplo 1: definir a permissão octal para um item</span><span class="sxs-lookup"><span data-stu-id="030d3-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="030d3-109">Esse comando define o octal de permissão de um arquivo para 0770, que traduz para limpar o bit adesivo, definindo as permissões de leitura/gravação/execução para o proprietário do arquivo, definindo as permissões de leitura/gravação/execução para o grupo proprietário do arquivo e desmarcando as permissões de leitura/gravação/execução para outros.</span><span class="sxs-lookup"><span data-stu-id="030d3-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="030d3-110">OS</span><span class="sxs-lookup"><span data-stu-id="030d3-110">PARAMETERS</span></span>

### <span data-ttu-id="030d3-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="030d3-111">-Account</span></span>
<span data-ttu-id="030d3-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="030d3-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="030d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="030d3-113">-DefaultProfile</span></span>
<span data-ttu-id="030d3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="030d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="030d3-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="030d3-115">-Path</span></span>
<span data-ttu-id="030d3-116">Especifica o caminho do repositório data Lake do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="030d3-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="030d3-117">-Permissão</span><span class="sxs-lookup"><span data-stu-id="030d3-117">-Permission</span></span>
<span data-ttu-id="030d3-118">As permissões a serem definidas para o arquivo ou pasta, expressa como um octal (por exemplo, ' 777 ')</span><span class="sxs-lookup"><span data-stu-id="030d3-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

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

### <span data-ttu-id="030d3-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="030d3-119">-Confirm</span></span>
<span data-ttu-id="030d3-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="030d3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="030d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="030d3-121">-WhatIf</span></span>
<span data-ttu-id="030d3-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="030d3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="030d3-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="030d3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="030d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="030d3-124">CommonParameters</span></span>
<span data-ttu-id="030d3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="030d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="030d3-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="030d3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="030d3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="030d3-127">INPUTS</span></span>

### <span data-ttu-id="030d3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="030d3-128">System.String</span></span>

### <span data-ttu-id="030d3-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="030d3-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="030d3-130">System. Int32</span><span class="sxs-lookup"><span data-stu-id="030d3-130">System.Int32</span></span>

## <span data-ttu-id="030d3-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="030d3-131">OUTPUTS</span></span>

### <span data-ttu-id="030d3-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="030d3-132">System.Boolean</span></span>

## <span data-ttu-id="030d3-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="030d3-133">NOTES</span></span>
* <span data-ttu-id="030d3-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="030d3-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="030d3-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="030d3-135">RELATED LINKS</span></span>

[<span data-ttu-id="030d3-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="030d3-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


