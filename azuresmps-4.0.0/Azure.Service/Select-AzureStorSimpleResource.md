---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945448"
---
# <span data-ttu-id="47b9e-101">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="47b9e-101">Select-AzureStorSimpleResource</span></span>

## <span data-ttu-id="47b9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="47b9e-103">Define um recurso como o recurso atual.</span><span class="sxs-lookup"><span data-stu-id="47b9e-103">Sets a resource as the current resource.</span></span>

## <span data-ttu-id="47b9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47b9e-104">SYNTAX</span></span>

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="47b9e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47b9e-105">DESCRIPTION</span></span>
<span data-ttu-id="47b9e-106">O cmdlet **Select-AzureStorSimpleResource** define um recurso como o recurso atual.</span><span class="sxs-lookup"><span data-stu-id="47b9e-106">The **Select-AzureStorSimpleResource** cmdlet sets a resource as the current resource.</span></span>
<span data-ttu-id="47b9e-107">Depois de selecionar um recurso, outros cmdlets se aplicam ao contexto do recurso.</span><span class="sxs-lookup"><span data-stu-id="47b9e-107">After you select a resource, other cmdlets apply within that resource context.</span></span>

## <span data-ttu-id="47b9e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47b9e-108">EXAMPLES</span></span>

### <span data-ttu-id="47b9e-109">Exemplo 1: selecionar um recurso pela primeira vez</span><span class="sxs-lookup"><span data-stu-id="47b9e-109">Example 1: Select a resource for the first time</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="47b9e-110">Esse comando seleciona o recurso chamado Contoso64-Tsqa como o contexto atual.</span><span class="sxs-lookup"><span data-stu-id="47b9e-110">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="47b9e-111">Neste exemplo, o computador não tinha esse contexto inicializado anteriormente e, portanto, você deve especificar um valor para o parâmetro *RegistrationKey* .</span><span class="sxs-lookup"><span data-stu-id="47b9e-111">In this example, the computer has not had this context initialized previously, and, therefore, you must specify a value for the *RegistrationKey* parameter.</span></span>

### <span data-ttu-id="47b9e-112">Exemplo 2: tentativa de selecionar um recurso</span><span class="sxs-lookup"><span data-stu-id="47b9e-112">Example 2: Attempt to select a resource</span></span>
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### <span data-ttu-id="47b9e-113">Exemplo 3: selecionar um recurso selecionado anteriormente</span><span class="sxs-lookup"><span data-stu-id="47b9e-113">Example 3: Select a previously selected resource</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="47b9e-114">Esse comando seleciona o recurso chamado Contoso64-Tsqa como o contexto atual.</span><span class="sxs-lookup"><span data-stu-id="47b9e-114">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="47b9e-115">Neste exemplo, esse contexto foi selecionado anteriormente e, portanto, você não precisa especificar um valor para o parâmetro *RegistrationKey* .</span><span class="sxs-lookup"><span data-stu-id="47b9e-115">In this example, that context has previously been selected, and, therefore, you do not need to specify a value for the *RegistrationKey* parameter.</span></span>

## <span data-ttu-id="47b9e-116">OS</span><span class="sxs-lookup"><span data-stu-id="47b9e-116">PARAMETERS</span></span>

### <span data-ttu-id="47b9e-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="47b9e-117">-Profile</span></span>
<span data-ttu-id="47b9e-118">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="47b9e-118">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b9e-119">-RegistrationKey</span><span class="sxs-lookup"><span data-stu-id="47b9e-119">-RegistrationKey</span></span>
<span data-ttu-id="47b9e-120">Especifica uma chave de registro.</span><span class="sxs-lookup"><span data-stu-id="47b9e-120">Specifies a registration key.</span></span>
<span data-ttu-id="47b9e-121">Especifique uma chave na primeira vez em que você selecionar um recurso.</span><span class="sxs-lookup"><span data-stu-id="47b9e-121">Specify a key the first time that you select a resource.</span></span>
<span data-ttu-id="47b9e-122">Depois que esse cmdlet seleciona o recurso atual, os cmdlets usam essa chave, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="47b9e-122">After this cmdlet selects the current resource, cmdlets use this key, as required.</span></span>
<span data-ttu-id="47b9e-123">Para obter mais informações, consulte [obter a chave de registro de serviço](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) na Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="47b9e-123">For more information, see [Get the service registration key](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) on the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b9e-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="47b9e-124">-ResourceName</span></span>
<span data-ttu-id="47b9e-125">Especifica o nome do recurso a ser selecionado como o recurso atual.</span><span class="sxs-lookup"><span data-stu-id="47b9e-125">Specifies the name of the resource to select as the current resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b9e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b9e-126">CommonParameters</span></span>
<span data-ttu-id="47b9e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b9e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b9e-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b9e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b9e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47b9e-129">INPUTS</span></span>

### <span data-ttu-id="47b9e-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="47b9e-130">None</span></span>

## <span data-ttu-id="47b9e-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47b9e-131">OUTPUTS</span></span>

### <span data-ttu-id="47b9e-132">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="47b9e-132">StorSimpleResourceContext</span></span>
<span data-ttu-id="47b9e-133">Esse cmdlet retorna um objeto **StorSimpleResourceContext** que contém detalhes do contexto do recurso.</span><span class="sxs-lookup"><span data-stu-id="47b9e-133">This cmdlet returns a **StorSimpleResourceContext** object that contains details for the resource context.</span></span>

## <span data-ttu-id="47b9e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47b9e-134">NOTES</span></span>

## <span data-ttu-id="47b9e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47b9e-135">RELATED LINKS</span></span>

[<span data-ttu-id="47b9e-136">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="47b9e-136">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="47b9e-137">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="47b9e-137">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)


