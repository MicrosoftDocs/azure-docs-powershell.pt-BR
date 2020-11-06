---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 94f81e8256af9282cdd5e09c1ab2822bf99c772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610505"
---
# <span data-ttu-id="a5f8c-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="a5f8c-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="a5f8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f8c-103">Modifica a ACL de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5f8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5f8c-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5f8c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5f8c-105">DESCRIPTION</span></span>
<span data-ttu-id="a5f8c-106">O cmdlet **set-AzureRmDataLakeStoreItemAcl** modifica a ACL (lista de controle de acesso) de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a5f8c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5f8c-107">EXAMPLES</span></span>

### <span data-ttu-id="a5f8c-108">Exemplo 1: definir a ACL para um arquivo e uma pasta</span><span class="sxs-lookup"><span data-stu-id="a5f8c-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="a5f8c-109">O primeiro comando obtém a ACL para o diretório raiz da conta do ContosoADL e, em seguida, armazena-o na variável $ACL.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="a5f8c-110">O segundo comando define a ACL do arquivo Test.txt como a do $ACL.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="a5f8c-111">OS</span><span class="sxs-lookup"><span data-stu-id="a5f8c-111">PARAMETERS</span></span>

### <span data-ttu-id="a5f8c-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="a5f8c-112">-Account</span></span>
<span data-ttu-id="a5f8c-113">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a5f8c-114">-ACL</span><span class="sxs-lookup"><span data-stu-id="a5f8c-114">-Acl</span></span>
<span data-ttu-id="a5f8c-115">Especifica uma ACL para um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f8c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5f8c-116">-PassThru</span></span>
<span data-ttu-id="a5f8c-117">Indica que a ACL resultante deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-117">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f8c-118">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a5f8c-118">-Path</span></span>
<span data-ttu-id="a5f8c-119">Especifica o caminho do repositório data Lake do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="a5f8c-119">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a5f8c-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5f8c-120">-Confirm</span></span>
<span data-ttu-id="a5f8c-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5f8c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5f8c-122">-WhatIf</span></span>
<span data-ttu-id="a5f8c-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5f8c-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5f8c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f8c-125">-DefaultProfile</span></span>
<span data-ttu-id="a5f8c-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5f8c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f8c-127">CommonParameters</span></span>
<span data-ttu-id="a5f8c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f8c-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5f8c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f8c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5f8c-130">INPUTS</span></span>

### <span data-ttu-id="a5f8c-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="a5f8c-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="a5f8c-132">O parâmetro ' ACL ' aceita o valor do tipo ' DataLakeStoreItemAce [] ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a5f8c-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="a5f8c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5f8c-133">OUTPUTS</span></span>

### <span data-ttu-id="a5f8c-134">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="a5f8c-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="a5f8c-135">Se PassThru for especificado, retornará a lista resultante de entradas ACL.</span><span class="sxs-lookup"><span data-stu-id="a5f8c-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="a5f8c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5f8c-136">NOTES</span></span>

## <span data-ttu-id="a5f8c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5f8c-137">RELATED LINKS</span></span>

