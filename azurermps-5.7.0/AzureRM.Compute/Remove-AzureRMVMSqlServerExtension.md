---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: f074d61919098d6c23ab39424774d9ba18e457d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427614"
---
# <span data-ttu-id="afb69-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="afb69-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="afb69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afb69-102">SYNOPSIS</span></span>
<span data-ttu-id="afb69-103">Remove uma extensão do SQL Server de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="afb69-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afb69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afb69-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="afb69-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afb69-105">DESCRIPTION</span></span>
<span data-ttu-id="afb69-106">O cmdlet **Remove-AzureRmVMSqlServerExtension** remove uma extensão de servidor AzureSQL de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="afb69-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="afb69-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afb69-107">EXAMPLES</span></span>

### <span data-ttu-id="afb69-108">Exemplo 1: remover uma extensão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="afb69-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="afb69-109">Esse comando Remove uma extensão do SQL Server da máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="afb69-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="afb69-110">OS</span><span class="sxs-lookup"><span data-stu-id="afb69-110">PARAMETERS</span></span>

### <span data-ttu-id="afb69-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="afb69-111">-Name</span></span>
<span data-ttu-id="afb69-112">Especifica o nome do SQL Server que a extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="afb69-112">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb69-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb69-113">-ResourceGroupName</span></span>
<span data-ttu-id="afb69-114">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="afb69-114">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb69-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="afb69-115">-VMName</span></span>
<span data-ttu-id="afb69-116">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="afb69-116">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb69-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb69-117">CommonParameters</span></span>
<span data-ttu-id="afb69-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb69-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb69-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb69-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb69-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afb69-120">INPUTS</span></span>

### <span data-ttu-id="afb69-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="afb69-121">None</span></span>
<span data-ttu-id="afb69-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="afb69-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="afb69-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afb69-123">OUTPUTS</span></span>

## <span data-ttu-id="afb69-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afb69-124">NOTES</span></span>

## <span data-ttu-id="afb69-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afb69-125">RELATED LINKS</span></span>

[<span data-ttu-id="afb69-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="afb69-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="afb69-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="afb69-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


