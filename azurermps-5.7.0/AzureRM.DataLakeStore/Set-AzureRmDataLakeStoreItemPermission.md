---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 82dac83b9e252e154cedb50f7a3b90a1a78c01c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432134"
---
# <span data-ttu-id="ddcfe-101">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="ddcfe-101">Set-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="ddcfe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ddcfe-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcfe-103">Modifica a permissão octal de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddcfe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddcfe-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Permission] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddcfe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ddcfe-105">DESCRIPTION</span></span>
<span data-ttu-id="ddcfe-106">O cmdlet **set-AzureRmDataLakeStoreItemPermission** modifica a permissão octal de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-106">The **Set-AzureRmDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ddcfe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddcfe-107">EXAMPLES</span></span>

### <span data-ttu-id="ddcfe-108">Exemplo 1: definir a permissão octal para um item</span><span class="sxs-lookup"><span data-stu-id="ddcfe-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="ddcfe-109">Esse comando define o octal de permissão de um arquivo para 0770, que traduz para limpar o bit adesivo, definindo as permissões de leitura/gravação/execução para o proprietário do arquivo, definindo as permissões de leitura/gravação/execução para o grupo proprietário do arquivo e desmarcando as permissões de leitura/gravação/execução para outros.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="ddcfe-110">OS</span><span class="sxs-lookup"><span data-stu-id="ddcfe-110">PARAMETERS</span></span>

### <span data-ttu-id="ddcfe-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="ddcfe-111">-Account</span></span>
<span data-ttu-id="ddcfe-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="ddcfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddcfe-113">-DefaultProfile</span></span>
<span data-ttu-id="ddcfe-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddcfe-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="ddcfe-115">-Path</span></span>
<span data-ttu-id="ddcfe-116">Especifica o caminho do repositório data Lake do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="ddcfe-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ddcfe-117">-Permissão</span><span class="sxs-lookup"><span data-stu-id="ddcfe-117">-Permission</span></span>
<span data-ttu-id="ddcfe-118">As permissões a serem definidas para o arquivo ou pasta, expressa como um octal (por exemplo, ' 777 ')</span><span class="sxs-lookup"><span data-stu-id="ddcfe-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcfe-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ddcfe-119">-Confirm</span></span>
<span data-ttu-id="ddcfe-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcfe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddcfe-121">-WhatIf</span></span>
<span data-ttu-id="ddcfe-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddcfe-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcfe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcfe-124">CommonParameters</span></span>
<span data-ttu-id="ddcfe-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcfe-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddcfe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcfe-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ddcfe-127">INPUTS</span></span>

### <span data-ttu-id="ddcfe-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ddcfe-128">None</span></span>
<span data-ttu-id="ddcfe-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ddcfe-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ddcfe-130">OUTPUTS</span></span>

### <span data-ttu-id="ddcfe-131">bool</span><span class="sxs-lookup"><span data-stu-id="ddcfe-131">bool</span></span>
<span data-ttu-id="ddcfe-132">Retorna verdadeiro após a atualização com êxito da permissão.</span><span class="sxs-lookup"><span data-stu-id="ddcfe-132">Returns true upon successfully updating the permission.</span></span>

## <span data-ttu-id="ddcfe-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ddcfe-133">NOTES</span></span>
* <span data-ttu-id="ddcfe-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="ddcfe-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="ddcfe-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddcfe-135">RELATED LINKS</span></span>

[<span data-ttu-id="ddcfe-136">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="ddcfe-136">Get-AzureRmDataLakeStoreItemPermission</span></span>](./Get-AzureRmDataLakeStoreItemPermission.md)


