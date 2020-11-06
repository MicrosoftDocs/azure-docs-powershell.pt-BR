---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 630df5bbe6677c7019d372a2a6977cc4c724a421
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601274"
---
# <span data-ttu-id="6b6ec-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6b6ec-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="6b6ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6ec-103">Remove uma extensão do SQL Server de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="6b6ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b6ec-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b6ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b6ec-105">DESCRIPTION</span></span>
<span data-ttu-id="6b6ec-106">O cmdlet **Remove-AzVMSqlServerExtension** remove uma extensão de servidor AzureSQL de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="6b6ec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b6ec-107">EXAMPLES</span></span>

### <span data-ttu-id="6b6ec-108">Exemplo 1: remover uma extensão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="6b6ec-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="6b6ec-109">Esse comando Remove uma extensão do SQL Server da máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="6b6ec-110">OS</span><span class="sxs-lookup"><span data-stu-id="6b6ec-110">PARAMETERS</span></span>

### <span data-ttu-id="6b6ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6ec-111">-DefaultProfile</span></span>
<span data-ttu-id="6b6ec-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b6ec-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b6ec-113">-Name</span></span>
<span data-ttu-id="6b6ec-114">Especifica o nome do SQL Server que a extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6b6ec-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b6ec-115">-ResourceGroupName</span></span>
<span data-ttu-id="6b6ec-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6b6ec-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="6b6ec-117">-VMName</span></span>
<span data-ttu-id="6b6ec-118">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="6b6ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6ec-119">CommonParameters</span></span>
<span data-ttu-id="6b6ec-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b6ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6ec-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b6ec-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6ec-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b6ec-122">INPUTS</span></span>

### <span data-ttu-id="6b6ec-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6b6ec-123">System.String</span></span>

## <span data-ttu-id="6b6ec-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b6ec-124">OUTPUTS</span></span>

### <span data-ttu-id="6b6ec-125">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6b6ec-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6b6ec-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b6ec-126">NOTES</span></span>

## <span data-ttu-id="6b6ec-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b6ec-127">RELATED LINKS</span></span>

[<span data-ttu-id="6b6ec-128">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6b6ec-128">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="6b6ec-129">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6b6ec-129">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


