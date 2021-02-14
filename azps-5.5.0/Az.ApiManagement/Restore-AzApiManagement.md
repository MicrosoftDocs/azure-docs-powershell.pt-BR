---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116005"
---
# <span data-ttu-id="9095b-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9095b-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="9095b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9095b-102">SYNOPSIS</span></span>
<span data-ttu-id="9095b-103">Restaura um Serviço de Gerenciamento de API a partir do blob de armazenamento especificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="9095b-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="9095b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9095b-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9095b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9095b-105">DESCRIPTION</span></span>
<span data-ttu-id="9095b-106">O cmdlet **Restore-AzApiManagement** restaura um Serviço de Gerenciamento de API do backup especificado que reside em um blob do Azurestorage.</span><span class="sxs-lookup"><span data-stu-id="9095b-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="9095b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9095b-107">EXAMPLES</span></span>

### <span data-ttu-id="9095b-108">Exemplo 1: Restaurar um serviço de Gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="9095b-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="9095b-109">Esse comando restaura um serviço de Gerenciamento de API a partir do blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9095b-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="9095b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9095b-110">PARAMETERS</span></span>

### <span data-ttu-id="9095b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9095b-111">-DefaultProfile</span></span>
<span data-ttu-id="9095b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9095b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9095b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9095b-113">-Name</span></span>
<span data-ttu-id="9095b-114">Especifica o nome da instância de Gerenciamento de API que será restaurada com o backup.</span><span class="sxs-lookup"><span data-stu-id="9095b-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="9095b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9095b-115">-PassThru</span></span>
<span data-ttu-id="9095b-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9095b-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9095b-117">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="9095b-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9095b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9095b-118">-ResourceGroupName</span></span>
<span data-ttu-id="9095b-119">Especifica o nome do grupo de recursos no qual existe o Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="9095b-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="9095b-120">-SourceBname</span><span class="sxs-lookup"><span data-stu-id="9095b-120">-SourceBlobName</span></span>
<span data-ttu-id="9095b-121">Especifica o nome do blob de origem de backup de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9095b-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="9095b-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="9095b-122">-SourceContainerName</span></span>
<span data-ttu-id="9095b-123">Especifica o nome do contêiner de origem de backup de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9095b-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="9095b-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="9095b-124">-StorageContext</span></span>
<span data-ttu-id="9095b-125">Especifica o contexto de conexão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9095b-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="9095b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9095b-126">CommonParameters</span></span>
<span data-ttu-id="9095b-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9095b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9095b-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9095b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9095b-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="9095b-129">INPUTS</span></span>

### <span data-ttu-id="9095b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9095b-130">System.String</span></span>

## <span data-ttu-id="9095b-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="9095b-131">OUTPUTS</span></span>

### <span data-ttu-id="9095b-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9095b-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9095b-133">Notas</span><span class="sxs-lookup"><span data-stu-id="9095b-133">NOTES</span></span>

## <span data-ttu-id="9095b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9095b-134">RELATED LINKS</span></span>

[<span data-ttu-id="9095b-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9095b-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="9095b-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9095b-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="9095b-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9095b-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="9095b-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9095b-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


