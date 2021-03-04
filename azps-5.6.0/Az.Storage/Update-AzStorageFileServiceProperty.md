---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: cb50a4fd4a50ee2f1d62a3abff338b7a4c77f4cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888038"
---
# <span data-ttu-id="3228d-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3228d-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="3228d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3228d-102">SYNOPSIS</span></span>
<span data-ttu-id="3228d-103">Modifica as propriedades de serviço do serviço arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3228d-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="3228d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3228d-104">SYNTAX</span></span>

### <span data-ttu-id="3228d-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3228d-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3228d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3228d-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3228d-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="3228d-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3228d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3228d-108">DESCRIPTION</span></span>
<span data-ttu-id="3228d-109">O cmdlet **Update-AzStorageFileServiceProperty** modifica as propriedades de serviço do serviço arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3228d-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="3228d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3228d-110">EXAMPLES</span></span>

### <span data-ttu-id="3228d-111">Exemplo 1: Habilitar softdelete de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="3228d-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName                            : mystorageaccount
ResourceGroupName                             : myresourcegroup
ShareDeleteRetentionPolicy.Enabled            : True
ShareDeleteRetentionPolicy.Days               : 5
```

<span data-ttu-id="3228d-112">Este comando habilita a exclusão de softdelete do compartilhamento de arquivos com dias de retenção como 5</span><span class="sxs-lookup"><span data-stu-id="3228d-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="3228d-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3228d-113">PARAMETERS</span></span>

### <span data-ttu-id="3228d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3228d-114">-DefaultProfile</span></span>
<span data-ttu-id="3228d-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3228d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3228d-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3228d-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="3228d-117">Habilita o compartilhamento Excluir Política de Retenção para a conta de armazenamento definida como $true, desabilite o compartilhamento Excluir Política de Retenção definida como $false.</span><span class="sxs-lookup"><span data-stu-id="3228d-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3228d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3228d-118">-ResourceGroupName</span></span>
<span data-ttu-id="3228d-119">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="3228d-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3228d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3228d-120">-ResourceId</span></span>
<span data-ttu-id="3228d-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span><span class="sxs-lookup"><span data-stu-id="3228d-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3228d-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="3228d-122">-ShareRetentionDays</span></span>
<span data-ttu-id="3228d-123">Define o número de dias de retenção para o compartilhamento DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="3228d-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="3228d-124">O valor só deve ser definido quando habilitar o compartilhamento Excluir Política de Retenção.</span><span class="sxs-lookup"><span data-stu-id="3228d-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3228d-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3228d-125">-StorageAccount</span></span>
<span data-ttu-id="3228d-126">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3228d-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3228d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3228d-127">-StorageAccountName</span></span>
<span data-ttu-id="3228d-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3228d-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3228d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3228d-129">-Confirm</span></span>
<span data-ttu-id="3228d-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3228d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3228d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3228d-131">-WhatIf</span></span>
<span data-ttu-id="3228d-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3228d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3228d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3228d-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3228d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3228d-134">CommonParameters</span></span>
<span data-ttu-id="3228d-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3228d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3228d-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3228d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3228d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3228d-137">INPUTS</span></span>

### <span data-ttu-id="3228d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3228d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3228d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3228d-139">System.String</span></span>

## <span data-ttu-id="3228d-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3228d-140">OUTPUTS</span></span>

### <span data-ttu-id="3228d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="3228d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="3228d-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="3228d-142">NOTES</span></span>

## <span data-ttu-id="3228d-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3228d-143">RELATED LINKS</span></span>
