---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114441"
---
# <span data-ttu-id="ced33-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ced33-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="ced33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ced33-102">SYNOPSIS</span></span>
<span data-ttu-id="ced33-103">Obtém propriedades de serviço para os serviços de Arquivo de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ced33-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="ced33-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ced33-104">SYNTAX</span></span>

### <span data-ttu-id="ced33-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ced33-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ced33-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ced33-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ced33-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="ced33-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ced33-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ced33-108">DESCRIPTION</span></span>
<span data-ttu-id="ced33-109">O cmdlet **Get-AzStorageFileServiceProperty** obtém as propriedades de serviço dos serviços de Arquivo de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ced33-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="ced33-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ced33-110">EXAMPLES</span></span>

### <span data-ttu-id="ced33-111">Exemplo 1: Obter a propriedade Serviços de Arquivo de Armazenamento do Azure de uma Conta de Armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="ced33-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="ced33-112">Esse comando obtém a propriedade Serviços de arquivo de uma Conta de Armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="ced33-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="ced33-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ced33-113">PARAMETERS</span></span>

### <span data-ttu-id="ced33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced33-114">-DefaultProfile</span></span>
<span data-ttu-id="ced33-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ced33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced33-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced33-116">-ResourceGroupName</span></span>
<span data-ttu-id="ced33-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ced33-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="ced33-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced33-118">-ResourceId</span></span>
<span data-ttu-id="ced33-119">Inserir uma ID de Recurso de conta de armazenamento ou uma ID de Recurso de propriedades do serviço de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ced33-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="ced33-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced33-120">-StorageAccount</span></span>
<span data-ttu-id="ced33-121">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ced33-121">Storage account object</span></span>

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

### <span data-ttu-id="ced33-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ced33-122">-StorageAccountName</span></span>
<span data-ttu-id="ced33-123">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ced33-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="ced33-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced33-124">CommonParameters</span></span>
<span data-ttu-id="ced33-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced33-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced33-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ced33-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced33-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="ced33-127">INPUTS</span></span>

### <span data-ttu-id="ced33-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ced33-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ced33-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ced33-129">System.String</span></span>

## <span data-ttu-id="ced33-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="ced33-130">OUTPUTS</span></span>

### <span data-ttu-id="ced33-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="ced33-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="ced33-132">Notas</span><span class="sxs-lookup"><span data-stu-id="ced33-132">NOTES</span></span>

## <span data-ttu-id="ced33-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ced33-133">RELATED LINKS</span></span>
