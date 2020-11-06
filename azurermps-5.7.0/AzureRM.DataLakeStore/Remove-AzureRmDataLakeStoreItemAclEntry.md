---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 41c1324c3762d0b6e04c0c532976c62c0a16067e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426714"
---
# <span data-ttu-id="9c345-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9c345-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="9c345-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c345-102">SYNOPSIS</span></span>
<span data-ttu-id="9c345-103">Remove uma entrada da ACL de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9c345-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c345-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c345-104">SYNTAX</span></span>

### <span data-ttu-id="9c345-105">RemoveByACLObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c345-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c345-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="9c345-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c345-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c345-107">DESCRIPTION</span></span>
<span data-ttu-id="9c345-108">O cmdlet **Remove-AzureRmDataLakeStoreItemAclEntry** remove uma Entry (ACE) da lista de controle de acesso (ACL) de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9c345-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9c345-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c345-109">EXAMPLES</span></span>

### <span data-ttu-id="9c345-110">Exemplo 1: remover uma entrada de usuário</span><span class="sxs-lookup"><span data-stu-id="9c345-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="9c345-111">Esse comando Remove a ACE do usuário para Patti Pereira da conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="9c345-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="9c345-112">OS</span><span class="sxs-lookup"><span data-stu-id="9c345-112">PARAMETERS</span></span>

### <span data-ttu-id="9c345-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="9c345-113">-Account</span></span>
<span data-ttu-id="9c345-114">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9c345-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9c345-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="9c345-115">-AceType</span></span>
<span data-ttu-id="9c345-116">Especifica o tipo de ACE a ser removida.</span><span class="sxs-lookup"><span data-stu-id="9c345-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="9c345-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9c345-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c345-118">Utilizador</span><span class="sxs-lookup"><span data-stu-id="9c345-118">User</span></span>
- <span data-ttu-id="9c345-119">Grupos</span><span class="sxs-lookup"><span data-stu-id="9c345-119">Group</span></span>
- <span data-ttu-id="9c345-120">Remoção</span><span class="sxs-lookup"><span data-stu-id="9c345-120">Mask</span></span>
- <span data-ttu-id="9c345-121">Demais</span><span class="sxs-lookup"><span data-stu-id="9c345-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: RemoveSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c345-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="9c345-122">-Acl</span></span>
<span data-ttu-id="9c345-123">Especifica o objeto ACL que contém as entradas a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="9c345-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c345-124">-Padrão</span><span class="sxs-lookup"><span data-stu-id="9c345-124">-Default</span></span>
<span data-ttu-id="9c345-125">Indica que essa operação Remove a ACE padrão da ACL especificada.</span><span class="sxs-lookup"><span data-stu-id="9c345-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c345-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c345-126">-DefaultProfile</span></span>
<span data-ttu-id="9c345-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c345-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c345-128">-ID</span><span class="sxs-lookup"><span data-stu-id="9c345-128">-Id</span></span>
<span data-ttu-id="9c345-129">Especifica a ID de objeto do usuário, grupo ou entidade de serviço do diretório do AzureActive para o qual remover uma ACE.</span><span class="sxs-lookup"><span data-stu-id="9c345-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c345-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c345-130">-PassThru</span></span>
<span data-ttu-id="9c345-131">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="9c345-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="9c345-132">-Caminho</span><span class="sxs-lookup"><span data-stu-id="9c345-132">-Path</span></span>
<span data-ttu-id="9c345-133">Especifica o caminho do repositório data Lake do item do qual você deseja remover uma ACE, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="9c345-133">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9c345-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c345-134">-Confirm</span></span>
<span data-ttu-id="9c345-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c345-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c345-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c345-136">-WhatIf</span></span>
<span data-ttu-id="9c345-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c345-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c345-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c345-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c345-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c345-139">CommonParameters</span></span>
<span data-ttu-id="9c345-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c345-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c345-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c345-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c345-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c345-142">INPUTS</span></span>

### <span data-ttu-id="9c345-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="9c345-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="9c345-144">O parâmetro ' ACL ' aceita o valor do tipo ' DataLakeStoreItemAce [] ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="9c345-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="9c345-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c345-145">OUTPUTS</span></span>

### <span data-ttu-id="9c345-146">bool</span><span class="sxs-lookup"><span data-stu-id="9c345-146">bool</span></span>
<span data-ttu-id="9c345-147">Se PassThru for especificado, retornará true após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9c345-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="9c345-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c345-148">NOTES</span></span>

## <span data-ttu-id="9c345-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c345-149">RELATED LINKS</span></span>

[<span data-ttu-id="9c345-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9c345-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


