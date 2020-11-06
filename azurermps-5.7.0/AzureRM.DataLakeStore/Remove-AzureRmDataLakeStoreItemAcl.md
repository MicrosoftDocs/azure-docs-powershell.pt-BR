---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 23eb57a6c12c3ce5ba8334b7309b5c282624620a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426711"
---
# <span data-ttu-id="93738-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="93738-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="93738-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93738-102">SYNOPSIS</span></span>
<span data-ttu-id="93738-103">Limpa a ACL de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="93738-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93738-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93738-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93738-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93738-105">DESCRIPTION</span></span>
<span data-ttu-id="93738-106">O cmdlet **Remove-AzureRmDataLakeStoreItemAcl** limpa a ACL (lista de controle de acesso) de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="93738-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="93738-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93738-107">EXAMPLES</span></span>

### <span data-ttu-id="93738-108">Exemplo 1: remover a ACL de uma pasta</span><span class="sxs-lookup"><span data-stu-id="93738-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="93738-109">Esse comando Remove a ACL do diretório raiz da conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="93738-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="93738-110">OS</span><span class="sxs-lookup"><span data-stu-id="93738-110">PARAMETERS</span></span>

### <span data-ttu-id="93738-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="93738-111">-Account</span></span>
<span data-ttu-id="93738-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93738-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="93738-113">-Padrão</span><span class="sxs-lookup"><span data-stu-id="93738-113">-Default</span></span>
<span data-ttu-id="93738-114">Indica que o cmdlet Remove a ACL padrão para um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="93738-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93738-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93738-115">-DefaultProfile</span></span>
<span data-ttu-id="93738-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93738-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93738-117">-Force</span><span class="sxs-lookup"><span data-stu-id="93738-117">-Force</span></span>
<span data-ttu-id="93738-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="93738-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93738-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93738-119">-PassThru</span></span>
<span data-ttu-id="93738-120">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="93738-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="93738-121">-Caminho</span><span class="sxs-lookup"><span data-stu-id="93738-121">-Path</span></span>
<span data-ttu-id="93738-122">Especifica o caminho do repositório data Lake do item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="93738-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="93738-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93738-123">-Confirm</span></span>
<span data-ttu-id="93738-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93738-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93738-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93738-125">-WhatIf</span></span>
<span data-ttu-id="93738-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93738-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93738-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93738-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93738-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93738-128">CommonParameters</span></span>
<span data-ttu-id="93738-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93738-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93738-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93738-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93738-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93738-131">INPUTS</span></span>

### <span data-ttu-id="93738-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="93738-132">None</span></span>
<span data-ttu-id="93738-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="93738-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93738-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93738-134">OUTPUTS</span></span>

### <span data-ttu-id="93738-135">bool</span><span class="sxs-lookup"><span data-stu-id="93738-135">bool</span></span>
<span data-ttu-id="93738-136">Se PassThru for especificado, retornará true após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="93738-136">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="93738-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93738-137">NOTES</span></span>
* <span data-ttu-id="93738-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="93738-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="93738-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93738-139">RELATED LINKS</span></span>

[<span data-ttu-id="93738-140">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="93738-140">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="93738-141">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="93738-141">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="93738-142">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="93738-142">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


