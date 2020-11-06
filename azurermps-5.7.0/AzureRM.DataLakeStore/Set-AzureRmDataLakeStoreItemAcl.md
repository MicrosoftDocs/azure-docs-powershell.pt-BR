---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 313813bec61dac2f5b41f7ad2d36e5ee5ba1b44f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428220"
---
# <span data-ttu-id="def41-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="def41-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="def41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="def41-102">SYNOPSIS</span></span>
<span data-ttu-id="def41-103">Modifica a ACL de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="def41-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="def41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="def41-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="def41-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="def41-105">DESCRIPTION</span></span>
<span data-ttu-id="def41-106">O cmdlet **set-AzureRmDataLakeStoreItemAcl** modifica a ACL (lista de controle de acesso) de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="def41-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="def41-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="def41-107">EXAMPLES</span></span>

### <span data-ttu-id="def41-108">Exemplo 1: definir a ACL para um arquivo e uma pasta</span><span class="sxs-lookup"><span data-stu-id="def41-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="def41-109">O primeiro comando obtém a ACL para o diretório raiz da conta do ContosoADL e, em seguida, armazena-o na variável $ACL.</span><span class="sxs-lookup"><span data-stu-id="def41-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="def41-110">O segundo comando define a ACL do arquivo Test.txt como a do $ACL.</span><span class="sxs-lookup"><span data-stu-id="def41-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="def41-111">OS</span><span class="sxs-lookup"><span data-stu-id="def41-111">PARAMETERS</span></span>

### <span data-ttu-id="def41-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="def41-112">-Account</span></span>
<span data-ttu-id="def41-113">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="def41-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="def41-114">-ACL</span><span class="sxs-lookup"><span data-stu-id="def41-114">-Acl</span></span>
<span data-ttu-id="def41-115">Especifica uma ACL para um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="def41-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="def41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def41-116">-DefaultProfile</span></span>
<span data-ttu-id="def41-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="def41-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="def41-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="def41-118">-PassThru</span></span>
<span data-ttu-id="def41-119">Indica que a ACL resultante deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="def41-119">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="def41-120">-Caminho</span><span class="sxs-lookup"><span data-stu-id="def41-120">-Path</span></span>
<span data-ttu-id="def41-121">Especifica o caminho do repositório data Lake do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="def41-121">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="def41-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="def41-122">-Confirm</span></span>
<span data-ttu-id="def41-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="def41-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="def41-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="def41-124">-WhatIf</span></span>
<span data-ttu-id="def41-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="def41-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="def41-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="def41-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="def41-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def41-127">CommonParameters</span></span>
<span data-ttu-id="def41-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def41-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def41-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="def41-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def41-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="def41-130">INPUTS</span></span>

### <span data-ttu-id="def41-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="def41-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="def41-132">O parâmetro ' ACL ' aceita o valor do tipo ' DataLakeStoreItemAce [] ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="def41-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="def41-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="def41-133">OUTPUTS</span></span>

### <span data-ttu-id="def41-134">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="def41-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="def41-135">Se PassThru for especificado, retornará a lista resultante de entradas ACL.</span><span class="sxs-lookup"><span data-stu-id="def41-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="def41-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="def41-136">NOTES</span></span>

## <span data-ttu-id="def41-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="def41-137">RELATED LINKS</span></span>

