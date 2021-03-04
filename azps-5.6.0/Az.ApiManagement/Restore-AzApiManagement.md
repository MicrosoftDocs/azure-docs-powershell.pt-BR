---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d1c7e1938d50e4a970dbec15568bc5cf10257639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892575"
---
# <span data-ttu-id="913f3-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="913f3-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="913f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913f3-102">SYNOPSIS</span></span>
<span data-ttu-id="913f3-103">Restaura um Serviço de Gerenciamento de API a partir do blob de armazenamento do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="913f3-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="913f3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="913f3-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="913f3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="913f3-105">DESCRIPTION</span></span>
<span data-ttu-id="913f3-106">O cmdlet **Restore-AzApiManagement** restaura um Serviço de Gerenciamento de API do backup especificado que reside em um blob Azurestorage.</span><span class="sxs-lookup"><span data-stu-id="913f3-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="913f3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="913f3-107">EXAMPLES</span></span>

### <span data-ttu-id="913f3-108">Exemplo 1: Restaurar um serviço de Gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="913f3-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="913f3-109">Este comando restaura um serviço de Gerenciamento de API do blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="913f3-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="913f3-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="913f3-110">PARAMETERS</span></span>

### <span data-ttu-id="913f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913f3-111">-DefaultProfile</span></span>
<span data-ttu-id="913f3-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="913f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="913f3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="913f3-113">-Name</span></span>
<span data-ttu-id="913f3-114">Especifica o nome da instância de Gerenciamento de API que será restaurada com o backup.</span><span class="sxs-lookup"><span data-stu-id="913f3-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="913f3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="913f3-115">-PassThru</span></span>
<span data-ttu-id="913f3-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="913f3-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="913f3-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="913f3-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="913f3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913f3-118">-ResourceGroupName</span></span>
<span data-ttu-id="913f3-119">Especifica o nome do grupo de recursos no qual existe o Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="913f3-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="913f3-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="913f3-120">-SourceBlobName</span></span>
<span data-ttu-id="913f3-121">Especifica o nome do blob de origem de backup de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="913f3-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="913f3-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="913f3-122">-SourceContainerName</span></span>
<span data-ttu-id="913f3-123">Especifica o nome do contêiner de origem de backup de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="913f3-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="913f3-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="913f3-124">-StorageContext</span></span>
<span data-ttu-id="913f3-125">Especifica o contexto de conexão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="913f3-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="913f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913f3-126">CommonParameters</span></span>
<span data-ttu-id="913f3-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="913f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913f3-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="913f3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913f3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="913f3-129">INPUTS</span></span>

### <span data-ttu-id="913f3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="913f3-130">System.String</span></span>

## <span data-ttu-id="913f3-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="913f3-131">OUTPUTS</span></span>

### <span data-ttu-id="913f3-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="913f3-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="913f3-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="913f3-133">NOTES</span></span>

## <span data-ttu-id="913f3-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="913f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="913f3-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="913f3-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="913f3-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="913f3-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="913f3-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="913f3-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="913f3-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="913f3-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


