---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: fc9d8db7f293ff94e33b50afd55176d157046fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431782"
---
# <span data-ttu-id="a73ff-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a73ff-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="a73ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a73ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a73ff-103">Obtém as credenciais de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="a73ff-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a73ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a73ff-104">SYNTAX</span></span>

### <span data-ttu-id="a73ff-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a73ff-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a73ff-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a73ff-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a73ff-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a73ff-107">DESCRIPTION</span></span>
<span data-ttu-id="a73ff-108">O cmdlet **Get-AzureRmContainerRegistryCredential** Obtém as credenciais de logon para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="a73ff-108">The **Get-AzureRmContainerRegistryCredential** cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="a73ff-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a73ff-109">EXAMPLES</span></span>

### <span data-ttu-id="a73ff-110">Exemplo 1: obter as credenciais de logon para um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="a73ff-110">Example 1: Get the login credentials for a container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="a73ff-111">Este comando obtém as credenciais de logon para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="a73ff-111">This command gets the login credentials for the specified container registry.</span></span> <span data-ttu-id="a73ff-112">O usuário administrador precisa estar habilitado para o registro do contêiner `MyRegistry` para obter credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="a73ff-112">Admin user has to be enabled for the container registry `MyRegistry` to get login credentials.</span></span>

## <span data-ttu-id="a73ff-113">OS</span><span class="sxs-lookup"><span data-stu-id="a73ff-113">PARAMETERS</span></span>

### <span data-ttu-id="a73ff-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a73ff-114">-Name</span></span>
<span data-ttu-id="a73ff-115">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a73ff-115">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73ff-116">-Registro</span><span class="sxs-lookup"><span data-stu-id="a73ff-116">-Registry</span></span>
<span data-ttu-id="a73ff-117">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a73ff-117">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a73ff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a73ff-118">-ResourceGroupName</span></span>
<span data-ttu-id="a73ff-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a73ff-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73ff-120">-DefaultProfile</span></span>
<span data-ttu-id="a73ff-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a73ff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a73ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73ff-122">CommonParameters</span></span>
<span data-ttu-id="a73ff-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a73ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73ff-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a73ff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73ff-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a73ff-125">INPUTS</span></span>

### <span data-ttu-id="a73ff-126">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a73ff-126">PSContainerRegistry</span></span>
<span data-ttu-id="a73ff-127">O parâmetro ' Registry ' aceita o valor do tipo ' PSContainerRegistry ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a73ff-127">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="a73ff-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a73ff-128">OUTPUTS</span></span>

### <span data-ttu-id="a73ff-129">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a73ff-129">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="a73ff-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a73ff-130">NOTES</span></span>

## <span data-ttu-id="a73ff-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a73ff-131">RELATED LINKS</span></span>

[<span data-ttu-id="a73ff-132">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a73ff-132">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="a73ff-133">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a73ff-133">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="a73ff-134">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a73ff-134">Update-AzureRmContainerRegistryCredential</span></span>](./Update-AzureRmContainerRegistryCredential.md)

