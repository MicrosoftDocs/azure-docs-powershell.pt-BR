---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272134"
---
# <span data-ttu-id="d9d95-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d9d95-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="d9d95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9d95-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d95-103">Restaura um serviço de gerenciamento de API do blob de armazenamento do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="d9d95-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="d9d95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9d95-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9d95-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9d95-105">DESCRIPTION</span></span>
<span data-ttu-id="d9d95-106">O cmdlet **Restore-AzApiManagement** restaura um serviço de gerenciamento de API do backup especificado que reside em um blob AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="d9d95-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="d9d95-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9d95-107">EXAMPLES</span></span>

### <span data-ttu-id="d9d95-108">Exemplo 1: restaurar um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="d9d95-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="d9d95-109">Esse comando restaura um serviço de gerenciamento de API do blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d95-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="d9d95-110">OS</span><span class="sxs-lookup"><span data-stu-id="d9d95-110">PARAMETERS</span></span>

### <span data-ttu-id="d9d95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d95-111">-DefaultProfile</span></span>
<span data-ttu-id="d9d95-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d95-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9d95-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9d95-113">-Name</span></span>
<span data-ttu-id="d9d95-114">Especifica o nome da instância de gerenciamento de API que será restaurada com o backup.</span><span class="sxs-lookup"><span data-stu-id="d9d95-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d95-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9d95-115">-PassThru</span></span>
<span data-ttu-id="d9d95-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d9d95-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d9d95-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d9d95-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d95-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d95-118">-ResourceGroupName</span></span>
<span data-ttu-id="d9d95-119">Especifica o nome do grupo de recursos sob o qual existe gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="d9d95-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d95-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="d9d95-120">-SourceBlobName</span></span>
<span data-ttu-id="d9d95-121">Especifica o nome do blob de fonte de backup do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d95-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d95-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="d9d95-122">-SourceContainerName</span></span>
<span data-ttu-id="d9d95-123">Especifica o nome do contêiner da fonte de backup do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d95-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d95-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="d9d95-124">-StorageContext</span></span>
<span data-ttu-id="d9d95-125">Especifica o contexto de conexão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d9d95-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d95-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d95-126">CommonParameters</span></span>
<span data-ttu-id="d9d95-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d95-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d95-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9d95-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d95-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9d95-129">INPUTS</span></span>

### <span data-ttu-id="d9d95-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d9d95-130">System.String</span></span>

## <span data-ttu-id="d9d95-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9d95-131">OUTPUTS</span></span>

### <span data-ttu-id="d9d95-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="d9d95-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="d9d95-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9d95-133">NOTES</span></span>

## <span data-ttu-id="d9d95-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9d95-134">RELATED LINKS</span></span>

[<span data-ttu-id="d9d95-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d9d95-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="d9d95-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d9d95-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="d9d95-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d9d95-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="d9d95-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d9d95-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


