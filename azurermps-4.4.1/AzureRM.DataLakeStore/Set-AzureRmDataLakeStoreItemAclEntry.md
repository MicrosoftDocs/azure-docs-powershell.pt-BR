---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 9646ef98499e56e24ce81c78f6b94dce75ff0078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440671"
---
# <span data-ttu-id="5b1a4-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5b1a4-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="5b1a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b1a4-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1a4-103">Modifica uma entrada na ACL de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b1a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b1a4-104">SYNTAX</span></span>

### <span data-ttu-id="5b1a4-105">Definir entradas ACL usando o objeto ACL (padrão)</span><span class="sxs-lookup"><span data-stu-id="5b1a4-105">Set ACL Entries using ACL object (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b1a4-106">Definir ACE específico</span><span class="sxs-lookup"><span data-stu-id="5b1a4-106">Set specific ACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b1a4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b1a4-107">DESCRIPTION</span></span>
<span data-ttu-id="5b1a4-108">O cmdlet **set-AzureRmDataLakeStoreItemAclEntry** modifica uma Entry (ACE) na lista de controle de acesso (ACL) de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5b1a4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b1a4-109">EXAMPLES</span></span>

### <span data-ttu-id="5b1a4-110">Exemplo 1: modificar permissões para uma ACE</span><span class="sxs-lookup"><span data-stu-id="5b1a4-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="5b1a4-111">Esse comando modifica a ACE para Patti Pereira para ter todas as permissões.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="5b1a4-112">OS</span><span class="sxs-lookup"><span data-stu-id="5b1a4-112">PARAMETERS</span></span>

### <span data-ttu-id="5b1a4-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="5b1a4-113">-Account</span></span>
<span data-ttu-id="5b1a4-114">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5b1a4-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="5b1a4-115">-AceType</span></span>
<span data-ttu-id="5b1a4-116">Especifica o tipo de ACE a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="5b1a4-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5b1a4-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b1a4-118">Utilizador</span><span class="sxs-lookup"><span data-stu-id="5b1a4-118">User</span></span> 
- <span data-ttu-id="5b1a4-119">Grupos</span><span class="sxs-lookup"><span data-stu-id="5b1a4-119">Group</span></span> 
- <span data-ttu-id="5b1a4-120">Remoção</span><span class="sxs-lookup"><span data-stu-id="5b1a4-120">Mask</span></span> 
- <span data-ttu-id="5b1a4-121">Demais</span><span class="sxs-lookup"><span data-stu-id="5b1a4-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Set specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1a4-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="5b1a4-122">-Acl</span></span>
<span data-ttu-id="5b1a4-123">Especifica o objeto ACL que contém as entradas a serem modificadas.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Set ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1a4-124">-Padrão</span><span class="sxs-lookup"><span data-stu-id="5b1a4-124">-Default</span></span>
<span data-ttu-id="5b1a4-125">Indica que essa operação modifica a ACE padrão da ACL especificada.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1a4-126">-ID</span><span class="sxs-lookup"><span data-stu-id="5b1a4-126">-Id</span></span>
<span data-ttu-id="5b1a4-127">Especifica a ID de objeto do usuário, grupo ou entidade de serviço do diretório do AzureActive para o qual modificar uma ACE.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1a4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b1a4-128">-PassThru</span></span>
<span data-ttu-id="5b1a4-129">Indica que a ACL resultante deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-129">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="5b1a4-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="5b1a4-130">-Path</span></span>
<span data-ttu-id="5b1a4-131">Especifica o caminho do repositório data Lake do item para o qual modificar uma ACE, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="5b1a4-131">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5b1a4-132">-Permissões</span><span class="sxs-lookup"><span data-stu-id="5b1a4-132">-Permissions</span></span>
<span data-ttu-id="5b1a4-133">Especifica as permissões para o ACE.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-133">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="5b1a4-134">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5b1a4-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b1a4-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5b1a4-135">None</span></span>
- <span data-ttu-id="5b1a4-136">Novamente</span><span class="sxs-lookup"><span data-stu-id="5b1a4-136">Execute</span></span>
- <span data-ttu-id="5b1a4-137">Gravação</span><span class="sxs-lookup"><span data-stu-id="5b1a4-137">Write</span></span>
- <span data-ttu-id="5b1a4-138">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="5b1a4-138">WriteExecute</span></span>
- <span data-ttu-id="5b1a4-139">Ler</span><span class="sxs-lookup"><span data-stu-id="5b1a4-139">Read</span></span>
- <span data-ttu-id="5b1a4-140">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="5b1a4-140">ReadExecute</span></span>
- <span data-ttu-id="5b1a4-141">Leitura</span><span class="sxs-lookup"><span data-stu-id="5b1a4-141">ReadWrite</span></span>
- <span data-ttu-id="5b1a4-142">Todo</span><span class="sxs-lookup"><span data-stu-id="5b1a4-142">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: Set specific ACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1a4-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5b1a4-143">-Confirm</span></span>
<span data-ttu-id="5b1a4-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1a4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b1a4-145">-WhatIf</span></span>
<span data-ttu-id="5b1a4-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b1a4-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1a4-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1a4-148">-DefaultProfile</span></span>
<span data-ttu-id="5b1a4-149">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b1a4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1a4-150">CommonParameters</span></span>
<span data-ttu-id="5b1a4-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1a4-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b1a4-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1a4-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b1a4-153">INPUTS</span></span>

### <span data-ttu-id="5b1a4-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="5b1a4-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="5b1a4-155">O parâmetro ' ACL ' aceita o valor do tipo ' DataLakeStoreItemAce [] ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="5b1a4-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="5b1a4-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b1a4-156">OUTPUTS</span></span>

### <span data-ttu-id="5b1a4-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="5b1a4-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="5b1a4-158">Se PassThru for especificado, retornará a lista resultante de entradas ACL.</span><span class="sxs-lookup"><span data-stu-id="5b1a4-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="5b1a4-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b1a4-159">NOTES</span></span>

## <span data-ttu-id="5b1a4-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b1a4-160">RELATED LINKS</span></span>

[<span data-ttu-id="5b1a4-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5b1a4-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


