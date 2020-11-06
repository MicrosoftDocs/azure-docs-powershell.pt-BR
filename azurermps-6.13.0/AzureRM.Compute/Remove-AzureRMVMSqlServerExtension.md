---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 83f697733d56ae7d99bc0b2660b5abbaca15a71f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440827"
---
# <span data-ttu-id="578ce-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="578ce-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="578ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="578ce-102">SYNOPSIS</span></span>
<span data-ttu-id="578ce-103">Remove uma extensão do SQL Server de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="578ce-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="578ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="578ce-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="578ce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="578ce-105">DESCRIPTION</span></span>
<span data-ttu-id="578ce-106">O cmdlet **Remove-AzureRmVMSqlServerExtension** remove uma extensão de servidor AzureSQL de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="578ce-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="578ce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="578ce-107">EXAMPLES</span></span>

### <span data-ttu-id="578ce-108">Exemplo 1: remover uma extensão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="578ce-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="578ce-109">Esse comando Remove uma extensão do SQL Server da máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="578ce-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="578ce-110">OS</span><span class="sxs-lookup"><span data-stu-id="578ce-110">PARAMETERS</span></span>

### <span data-ttu-id="578ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578ce-111">-DefaultProfile</span></span>
<span data-ttu-id="578ce-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="578ce-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="578ce-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="578ce-113">-Name</span></span>
<span data-ttu-id="578ce-114">Especifica o nome do SQL Server que a extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="578ce-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="578ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="578ce-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="578ce-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="578ce-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="578ce-117">-VMName</span></span>
<span data-ttu-id="578ce-118">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="578ce-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="578ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578ce-119">CommonParameters</span></span>
<span data-ttu-id="578ce-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="578ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578ce-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="578ce-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578ce-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="578ce-122">INPUTS</span></span>

### <span data-ttu-id="578ce-123">System. String</span><span class="sxs-lookup"><span data-stu-id="578ce-123">System.String</span></span>

## <span data-ttu-id="578ce-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="578ce-124">OUTPUTS</span></span>

### <span data-ttu-id="578ce-125">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="578ce-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="578ce-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="578ce-126">NOTES</span></span>

## <span data-ttu-id="578ce-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="578ce-127">RELATED LINKS</span></span>

[<span data-ttu-id="578ce-128">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="578ce-128">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="578ce-129">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="578ce-129">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


