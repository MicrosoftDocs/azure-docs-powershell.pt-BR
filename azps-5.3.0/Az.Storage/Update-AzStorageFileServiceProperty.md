---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427682"
---
# <span data-ttu-id="e5729-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e5729-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="e5729-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5729-102">SYNOPSIS</span></span>
<span data-ttu-id="e5729-103">Modifica as propriedades de serviço para o serviço de arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5729-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="e5729-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5729-104">SYNTAX</span></span>

### <span data-ttu-id="e5729-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e5729-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5729-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="e5729-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5729-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="e5729-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5729-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5729-108">DESCRIPTION</span></span>
<span data-ttu-id="e5729-109">O cmdlet **Update-AzStorageFileServiceProperty** modifica as propriedades de serviço para o serviço de arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5729-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="e5729-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5729-110">EXAMPLES</span></span>

### <span data-ttu-id="e5729-111">Exemplo 1: habilitar o compartilhamento de arquivos SoftDelete</span><span class="sxs-lookup"><span data-stu-id="e5729-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="e5729-112">Esse comando habilita o compartilhamento de arquivos SoftDelete excluir com dias de retenção como 5</span><span class="sxs-lookup"><span data-stu-id="e5729-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="e5729-113">OS</span><span class="sxs-lookup"><span data-stu-id="e5729-113">PARAMETERS</span></span>

### <span data-ttu-id="e5729-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5729-114">-DefaultProfile</span></span>
<span data-ttu-id="e5729-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5729-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5729-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5729-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="e5729-117">Habilite o compartilhamento excluir política de retenção para a conta de armazenamento definida como $true, desabilitar a política de retenção de exclusão de compartilhamento definida como $false.</span><span class="sxs-lookup"><span data-stu-id="e5729-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

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

### <span data-ttu-id="e5729-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5729-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5729-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5729-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="e5729-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5729-120">-ResourceId</span></span>
<span data-ttu-id="e5729-121">Insira uma ID de recurso da conta de armazenamento ou uma ID de recurso de propriedades do serviço de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e5729-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="e5729-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="e5729-122">-ShareRetentionDays</span></span>
<span data-ttu-id="e5729-123">Define o número de dias de retenção para o compartilhamento de DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="e5729-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="e5729-124">O valor só deve ser definido quando habilitar o compartilhamento excluir política de retenção.</span><span class="sxs-lookup"><span data-stu-id="e5729-124">The value should only be set when enable share Delete Retention Policy.</span></span>

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

### <span data-ttu-id="e5729-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5729-125">-StorageAccount</span></span>
<span data-ttu-id="e5729-126">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e5729-126">Storage account object</span></span>

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

### <span data-ttu-id="e5729-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e5729-127">-StorageAccountName</span></span>
<span data-ttu-id="e5729-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5729-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="e5729-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e5729-129">-Confirm</span></span>
<span data-ttu-id="e5729-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5729-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5729-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5729-131">-WhatIf</span></span>
<span data-ttu-id="e5729-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5729-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5729-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5729-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5729-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5729-134">CommonParameters</span></span>
<span data-ttu-id="e5729-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5729-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5729-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5729-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5729-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5729-137">INPUTS</span></span>

### <span data-ttu-id="e5729-138">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5729-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e5729-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e5729-139">System.String</span></span>

## <span data-ttu-id="e5729-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5729-140">OUTPUTS</span></span>

### <span data-ttu-id="e5729-141">Microsoft. Azure. Commands. Management. Storage. Models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="e5729-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="e5729-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5729-142">NOTES</span></span>

## <span data-ttu-id="e5729-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5729-143">RELATED LINKS</span></span>
