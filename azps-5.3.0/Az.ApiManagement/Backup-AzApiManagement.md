---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432761"
---
# <span data-ttu-id="f354b-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f354b-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="f354b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f354b-102">SYNOPSIS</span></span>
<span data-ttu-id="f354b-103">Faz backup de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f354b-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="f354b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f354b-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f354b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f354b-105">DESCRIPTION</span></span>
<span data-ttu-id="f354b-106">O cmdlet **backup-AzApiManagement** faz a cópia de um serviço de gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="f354b-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="f354b-107">Esse cmdlet armazena o backup como um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f354b-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="f354b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f354b-108">EXAMPLES</span></span>

### <span data-ttu-id="f354b-109">Exemplo 1: fazer backup de um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="f354b-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="f354b-110">Esse comando faz backup de um serviço de gerenciamento de API em um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f354b-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="f354b-111">OS</span><span class="sxs-lookup"><span data-stu-id="f354b-111">PARAMETERS</span></span>

### <span data-ttu-id="f354b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f354b-112">-DefaultProfile</span></span>
<span data-ttu-id="f354b-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f354b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f354b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="f354b-114">-Name</span></span>
<span data-ttu-id="f354b-115">Especifica o nome da implantação de gerenciamento de API que este cmdlet faz backup.</span><span class="sxs-lookup"><span data-stu-id="f354b-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="f354b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f354b-116">-PassThru</span></span>
<span data-ttu-id="f354b-117">Indica que esse cmdlet retorna o objeto **PsApiManagement** em backup, se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f354b-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="f354b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f354b-118">-ResourceGroupName</span></span>
<span data-ttu-id="f354b-119">Especifica o nome do grupo de recursos sob o qual existe a implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f354b-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="f354b-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="f354b-120">-StorageContext</span></span>
<span data-ttu-id="f354b-121">Especifica um contexto de conexão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f354b-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f354b-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="f354b-122">-TargetBlobName</span></span>
<span data-ttu-id="f354b-123">Especifica o nome do blob para o backup.</span><span class="sxs-lookup"><span data-stu-id="f354b-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="f354b-124">Se o BLOB não existir, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="f354b-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="f354b-125">Esse cmdlet gera um valor padrão com base no seguinte padrão: {Name}-{YYYY-MM-DD-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="f354b-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f354b-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="f354b-126">-TargetContainerName</span></span>
<span data-ttu-id="f354b-127">Especifica o nome do contêiner do blob para o backup.</span><span class="sxs-lookup"><span data-stu-id="f354b-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="f354b-128">Se o contêiner não existir, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="f354b-128">If the container does not exist, this cmdlet creates it.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f354b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f354b-129">CommonParameters</span></span>
<span data-ttu-id="f354b-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f354b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f354b-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f354b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f354b-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f354b-132">INPUTS</span></span>

### <span data-ttu-id="f354b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f354b-133">System.String</span></span>

### <span data-ttu-id="f354b-134">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f354b-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f354b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f354b-135">OUTPUTS</span></span>

### <span data-ttu-id="f354b-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f354b-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f354b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f354b-137">NOTES</span></span>

## <span data-ttu-id="f354b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f354b-138">RELATED LINKS</span></span>

[<span data-ttu-id="f354b-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f354b-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="f354b-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f354b-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="f354b-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f354b-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="f354b-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f354b-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


