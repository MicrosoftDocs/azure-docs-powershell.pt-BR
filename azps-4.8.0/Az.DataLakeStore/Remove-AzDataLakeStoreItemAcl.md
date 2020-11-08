---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112820"
---
# <span data-ttu-id="2bbc1-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="2bbc1-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="2bbc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bbc1-102">SYNOPSIS</span></span>
<span data-ttu-id="2bbc1-103">Limpa a ACL de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2bbc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bbc1-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bbc1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bbc1-105">DESCRIPTION</span></span>
<span data-ttu-id="2bbc1-106">O cmdlet **Remove-AzDataLakeStoreItemAcl** limpa a ACL (lista de controle de acesso) de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2bbc1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bbc1-107">EXAMPLES</span></span>

### <span data-ttu-id="2bbc1-108">Exemplo 1: remover a ACL de uma pasta</span><span class="sxs-lookup"><span data-stu-id="2bbc1-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="2bbc1-109">Esse comando Remove a ACL do diretório raiz da conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="2bbc1-110">OS</span><span class="sxs-lookup"><span data-stu-id="2bbc1-110">PARAMETERS</span></span>

### <span data-ttu-id="2bbc1-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="2bbc1-111">-Account</span></span>
<span data-ttu-id="2bbc1-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="2bbc1-113">-Padrão</span><span class="sxs-lookup"><span data-stu-id="2bbc1-113">-Default</span></span>
<span data-ttu-id="2bbc1-114">Indica que o cmdlet Remove a ACL padrão para um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bbc1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bbc1-115">-DefaultProfile</span></span>
<span data-ttu-id="2bbc1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bbc1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2bbc1-117">-Force</span></span>
<span data-ttu-id="2bbc1-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bbc1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bbc1-119">-PassThru</span></span>
<span data-ttu-id="2bbc1-120">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="2bbc1-121">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2bbc1-121">-Path</span></span>
<span data-ttu-id="2bbc1-122">Especifica o caminho do repositório data Lake do item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="2bbc1-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2bbc1-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2bbc1-123">-Confirm</span></span>
<span data-ttu-id="2bbc1-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bbc1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bbc1-125">-WhatIf</span></span>
<span data-ttu-id="2bbc1-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bbc1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bbc1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bbc1-128">CommonParameters</span></span>
<span data-ttu-id="2bbc1-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bbc1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bbc1-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bbc1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bbc1-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bbc1-131">INPUTS</span></span>

### <span data-ttu-id="2bbc1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2bbc1-132">System.String</span></span>

### <span data-ttu-id="2bbc1-133">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2bbc1-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2bbc1-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2bbc1-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2bbc1-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bbc1-135">OUTPUTS</span></span>

### <span data-ttu-id="2bbc1-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2bbc1-136">System.Boolean</span></span>

## <span data-ttu-id="2bbc1-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bbc1-137">NOTES</span></span>
* <span data-ttu-id="2bbc1-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="2bbc1-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="2bbc1-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bbc1-139">RELATED LINKS</span></span>

[<span data-ttu-id="2bbc1-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2bbc1-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="2bbc1-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="2bbc1-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="2bbc1-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2bbc1-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


